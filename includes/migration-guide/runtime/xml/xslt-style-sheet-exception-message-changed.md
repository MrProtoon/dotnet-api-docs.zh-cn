### <a name="xslt-style-sheet-exception-message-changed"></a><span data-ttu-id="0651b-101">更改的 XSLT 样式表异常消息</span><span class="sxs-lookup"><span data-stu-id="0651b-101">XSLT style sheet exception message changed</span></span>

|   |   |
|---|---|
|<span data-ttu-id="0651b-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="0651b-102">Details</span></span>|<span data-ttu-id="0651b-103">在.NET Framework 4.5 中，XSLT 文件过于复杂时的错误消息的文本是&quot;样式表太过复杂。&quot;在以前版本中，错误消息为&quot;XSLT 编译错误。&quot;取决于错误消息的文本的应用程序代码将不再有效。</span><span class="sxs-lookup"><span data-stu-id="0651b-103">In the .NET Framework 4.5, the text of the error message when an XSLT file is too complex is &quot;The style sheet is too complex.&quot; In previous versions, the error message was &quot;XSLT compile error.&quot; Application code that depends on the text of the error message will no longer work.</span></span> <span data-ttu-id="0651b-104">但是，异常类型保持不变，因此，此更改应该不会造成实际影响。</span><span class="sxs-lookup"><span data-stu-id="0651b-104">However, the exception types remain the same, so this change should have no real impact.</span></span>|
|<span data-ttu-id="0651b-105">建议</span><span class="sxs-lookup"><span data-stu-id="0651b-105">Suggestion</span></span>|<span data-ttu-id="0651b-106">更新任何应用程序代码，具体取决于从这种错误情况异常消息，需要新的消息，或 （甚至更好地） 更新代码以仅取决于异常类型 (<xref:System.Xml.Xsl.XsltException?displayProperty=name>)，这仍是如此。</span><span class="sxs-lookup"><span data-stu-id="0651b-106">Update any app code depending on the exception message from this error condition to expect the new message, or (even better) update the code to depend only on the exception type (<xref:System.Xml.Xsl.XsltException?displayProperty=name>), which has not changed.</span></span>|
|<span data-ttu-id="0651b-107">范围</span><span class="sxs-lookup"><span data-stu-id="0651b-107">Scope</span></span>|<span data-ttu-id="0651b-108">边缘</span><span class="sxs-lookup"><span data-stu-id="0651b-108">Edge</span></span>|
|<span data-ttu-id="0651b-109">版本</span><span class="sxs-lookup"><span data-stu-id="0651b-109">Version</span></span>|<span data-ttu-id="0651b-110">4.5</span><span class="sxs-lookup"><span data-stu-id="0651b-110">4.5</span></span>|
|<span data-ttu-id="0651b-111">类型</span><span class="sxs-lookup"><span data-stu-id="0651b-111">Type</span></span>|<span data-ttu-id="0651b-112">运行时</span><span class="sxs-lookup"><span data-stu-id="0651b-112">Runtime</span></span>|
|<span data-ttu-id="0651b-113">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="0651b-113">Affected APIs</span></span>|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|
