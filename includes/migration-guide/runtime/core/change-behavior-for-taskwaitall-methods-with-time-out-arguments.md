### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a><span data-ttu-id="dbd03-101">带超时自变量的 Task.WaitAll 方法的行为更改</span><span class="sxs-lookup"><span data-stu-id="dbd03-101">Change in behavior for Task.WaitAll methods with time-out arguments</span></span>

|   |   |
|---|---|
|<span data-ttu-id="dbd03-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="dbd03-102">Details</span></span>|<span data-ttu-id="dbd03-103">Task.WaitAll 行为是为了更加一致.NET 4.5.In.NET Framework 4 中，这些方法的行为不一致。</span><span class="sxs-lookup"><span data-stu-id="dbd03-103">Task.WaitAll behavior was made more consistent in .NET 4.5.In the .NET Framework 4, these methods behaved inconsistently.</span></span> <span data-ttu-id="dbd03-104">当超时到期时，如果在调用此方法之前已完成或已取消一个或多个任务，则此方法会引发 <xref:System.AggregateException?displayProperty=name> 异常。</span><span class="sxs-lookup"><span data-stu-id="dbd03-104">When the time-out expired, if one or more tasks were completed or canceled before the method call, the method threw an <xref:System.AggregateException?displayProperty=name> exception.</span></span> <span data-ttu-id="dbd03-105">在超时到期时，如果在调用此方法之前尚未完成或取消任何任务，但在调用此方法之后，一个或多个任务进入了这些状态，则该方法返回 false。</span><span class="sxs-lookup"><span data-stu-id="dbd03-105">When the time-out expired, if no tasks were completed or canceled before the method call, but one or more tasks entered these states after the method call, the method returned false.</span></span><br/><br/><span data-ttu-id="dbd03-106">在.NET Framework 4.5，这些方法重载现在时返回 false 的任何任务仍在运行时的超时间隔过期，并且它们将引发<xref:System.AggregateException?displayProperty=name>异常仅当取消某个输入的任务 （无论它是之前或之后方法调用） 和任何其他任务仍在运行。</span><span class="sxs-lookup"><span data-stu-id="dbd03-106">In the .NET Framework 4.5, these method overloads now return false if any tasks are still running when the time-out interval expired, and they throw an <xref:System.AggregateException?displayProperty=name> exception only if an input task was cancelled (regardless of whether it was before or after the method call) and no other tasks are still running.</span></span>|
|<span data-ttu-id="dbd03-107">建议</span><span class="sxs-lookup"><span data-stu-id="dbd03-107">Suggestion</span></span>|<span data-ttu-id="dbd03-108">如果<xref:System.AggregateException?displayProperty=name>正在捕获作为一种检测已取消正在调用 WaitAll 调用之前，代码应改为执行通过 IsCanceled 属性相同的检测的任务 (例如:。Any(t =&gt; t.IsCanceled)) 因为如果在超时之前完成所有等待的任务，仅将在这种情况下引发.NET 4.6。</span><span class="sxs-lookup"><span data-stu-id="dbd03-108">If an <xref:System.AggregateException?displayProperty=name> was being caught as a means of detecting a task that was cancelled prior to the WaitAll call being invoked, that code should instead do the same detection via the IsCanceled property (for example: .Any(t =&gt; t.IsCanceled)) since .NET 4.6 will only throw in that case if all awaited tasks are completed prior to the timeout.</span></span>|
|<span data-ttu-id="dbd03-109">范围</span><span class="sxs-lookup"><span data-stu-id="dbd03-109">Scope</span></span>|<span data-ttu-id="dbd03-110">次要</span><span class="sxs-lookup"><span data-stu-id="dbd03-110">Minor</span></span>|
|<span data-ttu-id="dbd03-111">版本</span><span class="sxs-lookup"><span data-stu-id="dbd03-111">Version</span></span>|<span data-ttu-id="dbd03-112">4.5</span><span class="sxs-lookup"><span data-stu-id="dbd03-112">4.5</span></span>|
|<span data-ttu-id="dbd03-113">类型</span><span class="sxs-lookup"><span data-stu-id="dbd03-113">Type</span></span>|<span data-ttu-id="dbd03-114">运行时</span><span class="sxs-lookup"><span data-stu-id="dbd03-114">Runtime</span></span>|
|<span data-ttu-id="dbd03-115">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="dbd03-115">Affected APIs</span></span>|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|
