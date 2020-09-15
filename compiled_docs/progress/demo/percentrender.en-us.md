{"title":"Custom Percentage","meta":{"title":"Custom Percentage","description":"\n<p>we can define how Percentage text to display by using <code>textRender</code>.\nThe exapme below will show a progressbar with accuracy of 2 decimal places and done icon when reached 100%.</p>\n","order":"7"},"codes":{"jsx":"import { Progress, Icon } from '@alifd/next';\n\nconst textRender = percent => {\n    if (percent === 100) {\n        return <Icon type=\"select\" size=\"medium\" />;\n    }\n    return `${percent.toFixed(2)}%`;\n};\n\nReactDOM.render(<div>\n    {[1, 2, 3, 4, 5, 6].map((value, index) => <Progress key={index} percent={value / 6 * 100} shape=\"circle\" color={`hsl(${index * 60 + 60}, 90%, 50%)`} textRender={textRender}/>)}\n    {[1, 2, 3, 4, 5, 6].map((value, index) => <Progress key={index} percent={value / 6 * 100} shape=\"line\" color={`hsl(${index * 60 + 60}, 90%, 50%)`} textRender={textRender}/>)}\n</div>, mountNode);\n"},"body":"\n````jsx\nimport { Progress, Icon } from '@alifd/next';\n\nconst textRender = percent => {\n    if (percent === 100) {\n        return <Icon type=\"select\" size=\"medium\" />;\n    }\n    return `${percent.toFixed(2)}%`;\n};\n\nReactDOM.render(<div>\n    {[1, 2, 3, 4, 5, 6].map((value, index) => <Progress key={index} percent={value / 6 * 100} shape=\"circle\" color={`hsl(${index * 60 + 60}, 90%, 50%)`} textRender={textRender}/>)}\n    {[1, 2, 3, 4, 5, 6].map((value, index) => <Progress key={index} percent={value / 6 * 100} shape=\"line\" color={`hsl(${index * 60 + 60}, 90%, 50%)`} textRender={textRender}/>)}\n</div>, mountNode);\n````","html":"<script>(function(){\"use strict\";\n\nvar _next = require(\"@alifd/next\");\n\nvar textRender = function textRender(percent) {\n    if (percent === 100) {\n        return React.createElement(_next.Icon, { type: \"select\", size: \"medium\" });\n    }\n    return percent.toFixed(2) + \"%\";\n};\n\nReactDOM.render(React.createElement(\n    \"div\",\n    null,\n    [1, 2, 3, 4, 5, 6].map(function (value, index) {\n        return React.createElement(_next.Progress, { key: index, percent: value / 6 * 100, shape: \"circle\", color: \"hsl(\" + (index * 60 + 60) + \", 90%, 50%)\", textRender: textRender });\n    }),\n    [1, 2, 3, 4, 5, 6].map(function (value, index) {\n        return React.createElement(_next.Progress, { key: index, percent: value / 6 * 100, shape: \"line\", color: \"hsl(\" + (index * 60 + 60) + \", 90%, 50%)\", textRender: textRender });\n    })\n), mountNode);})()</script><div class=\"highlight\"><pre class=\"language-jsx\"><code class=\"language-jsx\"><span class=\"token keyword\">import</span> <span class=\"token punctuation\">{</span> Progress<span class=\"token punctuation\">,</span> Icon <span class=\"token punctuation\">}</span> <span class=\"token keyword\">from</span> <span class=\"token string\">'@alifd/next'</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> <span class=\"token function-variable function\">textRender</span> <span class=\"token operator\">=</span> <span class=\"token parameter\">percent</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">{</span>\n    <span class=\"token keyword\">if</span> <span class=\"token punctuation\">(</span>percent <span class=\"token operator\">===</span> <span class=\"token number\">100</span><span class=\"token punctuation\">)</span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">return</span> <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span><span class=\"token class-name\">Icon</span></span> <span class=\"token attr-name\">type</span><span class=\"token attr-value\"><span class=\"token punctuation attr-equals\">=</span><span class=\"token punctuation\">\"</span>select<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">size</span><span class=\"token attr-value\"><span class=\"token punctuation attr-equals\">=</span><span class=\"token punctuation\">\"</span>medium<span class=\"token punctuation\">\"</span></span> <span class=\"token punctuation\">/></span></span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span>\n    <span class=\"token keyword\">return</span> <span class=\"token template-string\"><span class=\"token template-punctuation string\">`</span><span class=\"token interpolation\"><span class=\"token interpolation-punctuation punctuation\">${</span>percent<span class=\"token punctuation\">.</span><span class=\"token function\">toFixed</span><span class=\"token punctuation\">(</span><span class=\"token number\">2</span><span class=\"token punctuation\">)</span><span class=\"token interpolation-punctuation punctuation\">}</span></span><span class=\"token string\">%</span><span class=\"token template-punctuation string\">`</span></span><span class=\"token punctuation\">;</span>\n<span class=\"token punctuation\">}</span><span class=\"token punctuation\">;</span>\n\nReactDOM<span class=\"token punctuation\">.</span><span class=\"token function\">render</span><span class=\"token punctuation\">(</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>div</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n    </span><span class=\"token punctuation\">{</span><span class=\"token punctuation\">[</span><span class=\"token number\">1</span><span class=\"token punctuation\">,</span> <span class=\"token number\">2</span><span class=\"token punctuation\">,</span> <span class=\"token number\">3</span><span class=\"token punctuation\">,</span> <span class=\"token number\">4</span><span class=\"token punctuation\">,</span> <span class=\"token number\">5</span><span class=\"token punctuation\">,</span> <span class=\"token number\">6</span><span class=\"token punctuation\">]</span><span class=\"token punctuation\">.</span><span class=\"token function\">map</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">(</span><span class=\"token parameter\">value<span class=\"token punctuation\">,</span> index</span><span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span><span class=\"token class-name\">Progress</span></span> <span class=\"token attr-name\">key</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>index<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">percent</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>value <span class=\"token operator\">/</span> <span class=\"token number\">6</span> <span class=\"token operator\">*</span> <span class=\"token number\">100</span><span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">shape</span><span class=\"token attr-value\"><span class=\"token punctuation attr-equals\">=</span><span class=\"token punctuation\">\"</span>circle<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">color</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token template-string\"><span class=\"token template-punctuation string\">`</span><span class=\"token string\">hsl(</span><span class=\"token interpolation\"><span class=\"token interpolation-punctuation punctuation\">${</span>index <span class=\"token operator\">*</span> <span class=\"token number\">60</span> <span class=\"token operator\">+</span> <span class=\"token number\">60</span><span class=\"token interpolation-punctuation punctuation\">}</span></span><span class=\"token string\">, 90%, 50%)</span><span class=\"token template-punctuation string\">`</span></span><span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">textRender</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>textRender<span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">/></span></span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">}</span><span class=\"token plain-text\">\n    </span><span class=\"token punctuation\">{</span><span class=\"token punctuation\">[</span><span class=\"token number\">1</span><span class=\"token punctuation\">,</span> <span class=\"token number\">2</span><span class=\"token punctuation\">,</span> <span class=\"token number\">3</span><span class=\"token punctuation\">,</span> <span class=\"token number\">4</span><span class=\"token punctuation\">,</span> <span class=\"token number\">5</span><span class=\"token punctuation\">,</span> <span class=\"token number\">6</span><span class=\"token punctuation\">]</span><span class=\"token punctuation\">.</span><span class=\"token function\">map</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">(</span><span class=\"token parameter\">value<span class=\"token punctuation\">,</span> index</span><span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span><span class=\"token class-name\">Progress</span></span> <span class=\"token attr-name\">key</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>index<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">percent</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>value <span class=\"token operator\">/</span> <span class=\"token number\">6</span> <span class=\"token operator\">*</span> <span class=\"token number\">100</span><span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">shape</span><span class=\"token attr-value\"><span class=\"token punctuation attr-equals\">=</span><span class=\"token punctuation\">\"</span>line<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">color</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token template-string\"><span class=\"token template-punctuation string\">`</span><span class=\"token string\">hsl(</span><span class=\"token interpolation\"><span class=\"token interpolation-punctuation punctuation\">${</span>index <span class=\"token operator\">*</span> <span class=\"token number\">60</span> <span class=\"token operator\">+</span> <span class=\"token number\">60</span><span class=\"token interpolation-punctuation punctuation\">}</span></span><span class=\"token string\">, 90%, 50%)</span><span class=\"token template-punctuation string\">`</span></span><span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">textRender</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>textRender<span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">/></span></span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">}</span><span class=\"token plain-text\">\n</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>div</span><span class=\"token punctuation\">></span></span><span class=\"token punctuation\">,</span> mountNode<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span></code></pre></div>"}