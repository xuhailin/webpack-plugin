MinChunkSizePlugin	
"通过合并小于minChunkSize大小的chunk，将chunk体积保持在指定大小限制以上 设置最小分片条件"

LimitChunkCountPlugin	
"minChunksize:设置最小块大小。maxChunks：使用大于或等于最大的值限制块的最大数量设置分片限制"

AggressiveSplittingPlugin	
"可分割成较小的块，每个块超过maxSize,自动分块。它记录了webpack中的拆分点，能够恢复拆分。分片优化，
开启后会根据设定来合并分片代码"

HtmlWebpackPlugin	
生成一个html5文件，包括使用script标签的body中的所有webpack包，简化了html文件的创建。

BannerPlugin	为每个chunk文件头部添加banner

DllPlugin	"拆分bundles,提高构建速度，会创建一个manifest.json文件，用于DllReferencePlugin映射依赖关系。"

DllReferencePlugin	在webpack主配置文件中配置

DefinePlugin	允许创建一个在编译时可以配置的全局变量

EnvironmentPlugin 	通过DefinePlugin来设置process.env环境变量的快捷方式。

NamedModulesPlugin	建议用于开发，类似hashModelsIdsPulgin作用，生成相对路径

ExtractTextPlugin	
"分离样式，取出独立的css文件。将所有入口chunk中引用的css，移动到独立分离的css文件。
优点：更少的style标签。css SourceMap配置，css请求并行，css单独缓存，更快的游览器运行。
缺点：额外的http请求，编译时间更久，没有运行时的公共路径修改，没有热替换。"

HotModuleReplacementPlugin	启用热替换模块(HMR) 永远不要在生产环境下启用HMR!!可以在开发模式下启用。

HashedModuleIdsPlugin	
"建立用于生产模式，就是chunkname生成随机路径，main.aaaaaa.js
,aaaaaa就是随机数，第二次在部署，如果没有改变，就不会重新去打包"

ModuleConcatenationPlugin	部分提升，加快代码在游览器中的执行时间。

NoEmitOnErrorsPlugin	编译时遇到错误跳过发布阶段，确保不会出现包含错误的资源被发布

UglifyjsWebpackPlugin	压缩js

