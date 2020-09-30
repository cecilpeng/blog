## 初创团队技术选型

创业初期，技术团队必须花大力气确定技术选型。

这是一个多么痛的领悟。作为前端开发，曾经经历过混乱的技术栈：
1. 前端框架，包括Angular1、Vue、React
2. 跨端桌面应用，包括NW.js、Electron
3. 构建工具，包括fis3、webpack、vue-cli、rollup
4. 直播，包括腾讯trtc sdk，因为需要支持小程序
5. 自研，包括直播、IM

目前这些项目，个人都熟悉，也能正常维护。但是对于新入职的小伙伴来说，真是太难了——学习成本高，用法不标准，文档又少。

那么技术选型要怎么选呢？我觉得要着重考虑以下几点：

### 主流技术，丰富的生态

Vue/React目前是最主流的前端框架，发展到了相对成熟的阶段。而且，群众基础好，工具链完备，寻常问题都能在技术圈找到答案。对于大多数求职者，都能够胜任，招聘会变得容易。

跨端桌面应用，虽然之前一直在做NW.js，但是社区力量不足。尤其是，API能力不足、应用稳定性不足、第三方应用支持不足。比如，腾讯trtc、声网sdk就没有支持NW.js。怎么办？凉拌~当然，值得一说的是，NW.js入门门槛是低的。所以，一定坚持选Electron。

构建工具，是可以有更多尝试的，但是商用一定还是要选择主流稳定的。如果不统一，暂时也不要太担心，因为迁移成本相对较低。当然，不建议使用fis3（不维护）。

### 谨慎自研/选择开源，选择专业的第三方服务商

自研需要花费大量的精力，尤其是功能和稳定性是最容易出问题的。开源一般没有丰富的插件和应用支持，还是需要花费大量的精力。对于商用的项目，建议优先选择专业的第三方服务商，如果功能匹配，就看它是否足够纯粹、专注。

例如，选择直播sdk，建议选择声网，因为场景的覆盖会更深入，而非业务场景。举个例子，腾讯trtc，就没有flutter支持，Web支持也有限；声网还包括监控-水晶球、自定义-音视频云传输等更强大的能力。另外，直播的高集成解决方案是腾讯的一个发力点，如小程序直播、腾讯会议，这都证明了不够聚焦做基础服务。

### 团队匹配，前景较好

我熟悉Vue，对Vue底层原理也了解，那么，肯定是优先Vue、vue-cli。Vue目前有专业的团队一直维护核心库和文档社区，一直崇尚渐进式，向下兼容，前景良好。另外，vue-cli也准备更换vite，优化开发效率，我一直很喜欢~

团队暂时没有信任的app开发，所以自己必须肩负重任，熟悉app开发。对于web开发转app开发，最适合的还是flutter。那退路是什么呢？flutter可以构建UI层，也可以混合IOS、Android开发。如果非要做sdk，还是更建议使用IOS、Android，然后集成到flutter，因为目前市面主流还是app分IOS和Android两套。