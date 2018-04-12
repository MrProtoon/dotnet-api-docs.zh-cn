### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a><span data-ttu-id="2ab93-101">ObservableCollection ListBoxItem IsSelected 绑定问题&lt;T&gt;。移动</span><span class="sxs-lookup"><span data-stu-id="2ab93-101">ListBoxItem IsSelected binding issue with ObservableCollection&lt;T&gt;.Move</span></span>

|   |   |
|---|---|
|<span data-ttu-id="2ab93-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="2ab93-102">Details</span></span>|<span data-ttu-id="2ab93-103">调用<xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)>或<xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)>上绑定到的集合<xref:System.Windows.Controls.ListBox?displayProperty=name>其中选中项会导致不正常行为与将来的所选内容或的 unselection<xref:System.Windows.Controls.ListBox?displayProperty=name>项。</span><span class="sxs-lookup"><span data-stu-id="2ab93-103">Calling <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> or <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> on a collection bound to a <xref:System.Windows.Controls.ListBox?displayProperty=name> with items selected can lead to erratic behavior with future selection or unselection of <xref:System.Windows.Controls.ListBox?displayProperty=name> items.</span></span>|
|<span data-ttu-id="2ab93-104">建议</span><span class="sxs-lookup"><span data-stu-id="2ab93-104">Suggestion</span></span>|<span data-ttu-id="2ab93-105">调用<xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name>和<xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name>而不是<xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)>将解决此问题。</span><span class="sxs-lookup"><span data-stu-id="2ab93-105">Calling <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> and <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> instead of <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> will work around this issue.</span></span> <span data-ttu-id="2ab93-106">此外，此问题已在 .NET Framework 4.6 中解决，因此升级到该版本的 .NET Framework 即可解决该问题。</span><span class="sxs-lookup"><span data-stu-id="2ab93-106">Alternatively, this issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="2ab93-107">范围</span><span class="sxs-lookup"><span data-stu-id="2ab93-107">Scope</span></span>|<span data-ttu-id="2ab93-108">次要</span><span class="sxs-lookup"><span data-stu-id="2ab93-108">Minor</span></span>|
|<span data-ttu-id="2ab93-109">版本</span><span class="sxs-lookup"><span data-stu-id="2ab93-109">Version</span></span>|<span data-ttu-id="2ab93-110">4.5</span><span class="sxs-lookup"><span data-stu-id="2ab93-110">4.5</span></span>|
|<span data-ttu-id="2ab93-111">类型</span><span class="sxs-lookup"><span data-stu-id="2ab93-111">Type</span></span>|<span data-ttu-id="2ab93-112">运行时</span><span class="sxs-lookup"><span data-stu-id="2ab93-112">Runtime</span></span>|
|<span data-ttu-id="2ab93-113">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="2ab93-113">Affected APIs</span></span>|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|
