### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a><span data-ttu-id="01636-101">在注册表中注册自身时，.NET Framework 4.6 不使用 4.5.x.x 版本</span><span class="sxs-lookup"><span data-stu-id="01636-101">The .NET Framework 4.6 does not use a 4.5.x.x version when registering itself in the registry</span></span>

|   |   |
|---|---|
|<span data-ttu-id="01636-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="01636-102">Details</span></span>|<span data-ttu-id="01636-103">如您所料，在注册表中设置版本键 (在<code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) 的.NET Framework 4.6 开始"4.6"，而不"4.5"。</span><span class="sxs-lookup"><span data-stu-id="01636-103">As one might expect, the version key set in the registry (at <code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) for the .NET Framework 4.6 begins with '4.6', not '4.5'.</span></span> <span data-ttu-id="01636-104">应更新依赖于这些注册表项来了解在计算机上安装了哪些.NET Framework 版本的应用，以了解 4.6 是新的可能版本中，和一个与以前 4.5.x 兼容释放。</span><span class="sxs-lookup"><span data-stu-id="01636-104">Apps that depend on these registry keys to know which .NET Framework versions are installed on a machine should be updated to understand that 4.6 is a new possible version, and one that is compatible with previous 4.5.x releases.</span></span>|
|<span data-ttu-id="01636-105">建议</span><span class="sxs-lookup"><span data-stu-id="01636-105">Suggestion</span></span>|<span data-ttu-id="01636-106">通过查找 4.5 的注册表项来还接受 4.6 来安装更新应用探测的.NET Framework 4.5。</span><span class="sxs-lookup"><span data-stu-id="01636-106">Update apps probing for a .NET Framework 4.5 install by looking for 4.5 registry keys to also accept 4.6.</span></span>|
|<span data-ttu-id="01636-107">范围</span><span class="sxs-lookup"><span data-stu-id="01636-107">Scope</span></span>|<span data-ttu-id="01636-108">边缘</span><span class="sxs-lookup"><span data-stu-id="01636-108">Edge</span></span>|
|<span data-ttu-id="01636-109">版本</span><span class="sxs-lookup"><span data-stu-id="01636-109">Version</span></span>|<span data-ttu-id="01636-110">4.6</span><span class="sxs-lookup"><span data-stu-id="01636-110">4.6</span></span>|
|<span data-ttu-id="01636-111">类型</span><span class="sxs-lookup"><span data-stu-id="01636-111">Type</span></span>|<span data-ttu-id="01636-112">运行时</span><span class="sxs-lookup"><span data-stu-id="01636-112">Runtime</span></span>|
