{"title":"Basic","meta":{"title":"Basic","description":"\n<p><code>&lt;Consumer&gt;</code> can be to read context state of <code>&lt;ConfigProvider&gt;</code> with easly and highly customized</p>\n","order":"4"},"codes":{"jsx":"import { ConfigProvider } from '@alifd/next';\nimport PropTypes from 'prop-types';\n\nconst localeSettings = {\n    momentLocale: 'fr-FR',\n    CustomizedComponent: {\n        helloWorld: 'hello, world'\n    }\n};\n\nconst App = ({ children }) => (\n    <ConfigProvider\n        prefix=\"customized-\"\n        locale={localeSettings}\n        pure\n        warning={false}\n    >\n        {children}\n    </ConfigProvider>\n);\n\nApp.propTypes = {\n    children: PropTypes.node\n};\n\nconst Child = () => (\n    <ConfigProvider.Consumer>\n        {\n            context => (\n                <div className=\"context-data\">\n                    <h3>Context's state</h3>\n                    <pre>{JSON.stringify(context, false, 2)}</pre>\n                </div>\n            )\n        }\n    </ConfigProvider.Consumer>\n);\n\nconst Demo = () => (\n    <App>\n        <Child />\n    </App>\n);\n\nReactDOM.render(<Demo />, mountNode);\n","css":".context-data {\n    padding: 0 32px 32px;\n    border: 3px dashed #aaa;\n    border-radius: 9px;\n}\n"},"body":"\n````jsx\nimport { ConfigProvider } from '@alifd/next';\nimport PropTypes from 'prop-types';\n\nconst localeSettings = {\n    momentLocale: 'fr-FR',\n    CustomizedComponent: {\n        helloWorld: 'hello, world'\n    }\n};\n\nconst App = ({ children }) => (\n    <ConfigProvider\n        prefix=\"customized-\"\n        locale={localeSettings}\n        pure\n        warning={false}\n    >\n        {children}\n    </ConfigProvider>\n);\n\nApp.propTypes = {\n    children: PropTypes.node\n};\n\nconst Child = () => (\n    <ConfigProvider.Consumer>\n        {\n            context => (\n                <div className=\"context-data\">\n                    <h3>Context's state</h3>\n                    <pre>{JSON.stringify(context, false, 2)}</pre>\n                </div>\n            )\n        }\n    </ConfigProvider.Consumer>\n);\n\nconst Demo = () => (\n    <App>\n        <Child />\n    </App>\n);\n\nReactDOM.render(<Demo />, mountNode);\n````\n\n````css\n.context-data {\n    padding: 0 32px 32px;\n    border: 3px dashed #aaa;\n    border-radius: 9px;\n}\n````","html":"<script>(function(){'use strict';\n\nvar _next = require('@alifd/next');\n\nvar _propTypes = require('prop-types');\n\nvar _propTypes2 = _interopRequireDefault(_propTypes);\n\nfunction _interopRequireDefault(obj) { return obj && obj.__esModule ? obj : { default: obj }; }\n\nvar localeSettings = {\n    momentLocale: 'fr-FR',\n    CustomizedComponent: {\n        helloWorld: 'hello, world'\n    }\n};\n\nvar App = function App(_ref) {\n    var children = _ref.children;\n    return React.createElement(\n        _next.ConfigProvider,\n        {\n            prefix: 'customized-',\n            locale: localeSettings,\n            pure: true,\n            warning: false\n        },\n        children\n    );\n};\n\nApp.propTypes = {\n    children: _propTypes2.default.node\n};\n\nvar Child = function Child() {\n    return React.createElement(\n        _next.ConfigProvider.Consumer,\n        null,\n        function (context) {\n            return React.createElement(\n                'div',\n                { className: 'context-data' },\n                React.createElement(\n                    'h3',\n                    null,\n                    'Context\\'s state'\n                ),\n                React.createElement(\n                    'pre',\n                    null,\n                    JSON.stringify(context, false, 2)\n                )\n            );\n        }\n    );\n};\n\nvar Demo = function Demo() {\n    return React.createElement(\n        App,\n        null,\n        React.createElement(Child, null)\n    );\n};\n\nReactDOM.render(React.createElement(Demo, null), mountNode);})()</script><div class=\"highlight\"><pre class=\"language-jsx\"><code class=\"language-jsx\"><span class=\"token keyword\">import</span> <span class=\"token punctuation\">{</span> ConfigProvider <span class=\"token punctuation\">}</span> <span class=\"token keyword\">from</span> <span class=\"token string\">'@alifd/next'</span><span class=\"token punctuation\">;</span>\n<span class=\"token keyword\">import</span> PropTypes <span class=\"token keyword\">from</span> <span class=\"token string\">'prop-types'</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> localeSettings <span class=\"token operator\">=</span> <span class=\"token punctuation\">{</span>\n    momentLocale<span class=\"token operator\">:</span> <span class=\"token string\">'fr-FR'</span><span class=\"token punctuation\">,</span>\n    CustomizedComponent<span class=\"token operator\">:</span> <span class=\"token punctuation\">{</span>\n        helloWorld<span class=\"token operator\">:</span> <span class=\"token string\">'hello, world'</span>\n    <span class=\"token punctuation\">}</span>\n<span class=\"token punctuation\">}</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> <span class=\"token function-variable function\">App</span> <span class=\"token operator\">=</span> <span class=\"token punctuation\">(</span><span class=\"token parameter\"><span class=\"token punctuation\">{</span> children <span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">(</span>\n    <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span><span class=\"token class-name\">ConfigProvider</span></span>\n        <span class=\"token attr-name\">prefix</span><span class=\"token attr-value\"><span class=\"token punctuation attr-equals\">=</span><span class=\"token punctuation\">\"</span>customized-<span class=\"token punctuation\">\"</span></span>\n        <span class=\"token attr-name\">locale</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>localeSettings<span class=\"token punctuation\">}</span></span>\n        <span class=\"token attr-name\">pure</span>\n        <span class=\"token attr-name\">warning</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token boolean\">false</span><span class=\"token punctuation\">}</span></span>\n    <span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n        </span><span class=\"token punctuation\">{</span>children<span class=\"token punctuation\">}</span><span class=\"token plain-text\">\n    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span><span class=\"token class-name\">ConfigProvider</span></span><span class=\"token punctuation\">></span></span>\n<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n\nApp<span class=\"token punctuation\">.</span>propTypes <span class=\"token operator\">=</span> <span class=\"token punctuation\">{</span>\n    children<span class=\"token operator\">:</span> PropTypes<span class=\"token punctuation\">.</span>node\n<span class=\"token punctuation\">}</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> <span class=\"token function-variable function\">Child</span> <span class=\"token operator\">=</span> <span class=\"token punctuation\">(</span><span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">(</span>\n    <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span><span class=\"token class-name\">ConfigProvider.Consumer</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n        </span><span class=\"token punctuation\">{</span>\n            <span class=\"token parameter\">context</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">(</span>\n                <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>div</span> <span class=\"token attr-name\">className</span><span class=\"token attr-value\"><span class=\"token punctuation attr-equals\">=</span><span class=\"token punctuation\">\"</span>context-data<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>h3</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Context's state</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>h3</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>pre</span><span class=\"token punctuation\">></span></span><span class=\"token punctuation\">{</span><span class=\"token constant\">JSON</span><span class=\"token punctuation\">.</span><span class=\"token function\">stringify</span><span class=\"token punctuation\">(</span>context<span class=\"token punctuation\">,</span> <span class=\"token boolean\">false</span><span class=\"token punctuation\">,</span> <span class=\"token number\">2</span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">}</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>pre</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>div</span><span class=\"token punctuation\">></span></span>\n            <span class=\"token punctuation\">)</span>\n        <span class=\"token punctuation\">}</span><span class=\"token plain-text\">\n    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span><span class=\"token class-name\">ConfigProvider.Consumer</span></span><span class=\"token punctuation\">></span></span>\n<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> <span class=\"token function-variable function\">Demo</span> <span class=\"token operator\">=</span> <span class=\"token punctuation\">(</span><span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">(</span>\n    <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span><span class=\"token class-name\">App</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n        </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span><span class=\"token class-name\">Child</span></span> <span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span><span class=\"token class-name\">App</span></span><span class=\"token punctuation\">></span></span>\n<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n\nReactDOM<span class=\"token punctuation\">.</span><span class=\"token function\">render</span><span class=\"token punctuation\">(</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span><span class=\"token class-name\">Demo</span></span> <span class=\"token punctuation\">/></span></span><span class=\"token punctuation\">,</span> mountNode<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span></code></pre></div><style type=\"text/css\">.context-data {\n    padding: 0 32px 32px;\n    border: 3px dashed #aaa;\n    border-radius: 9px;\n}</style><div class=\"highlight\"><pre class=\"language-css\"><code class=\"language-css\"><span class=\"token selector\">.context-data</span> <span class=\"token punctuation\">{</span>\n    <span class=\"token property\">padding</span><span class=\"token punctuation\">:</span> 0 32px 32px<span class=\"token punctuation\">;</span>\n    <span class=\"token property\">border</span><span class=\"token punctuation\">:</span> 3px dashed #aaa<span class=\"token punctuation\">;</span>\n    <span class=\"token property\">border-radius</span><span class=\"token punctuation\">:</span> 9px<span class=\"token punctuation\">;</span>\n<span class=\"token punctuation\">}</span></code></pre></div>"}