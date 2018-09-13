# MyMvcPro

<h1 id="前端git版本库操作指南及规范"><a href="#" data-id="前端git版本库操作指南及规范" class="anchor"><span>前端Git版本库操作指南及规范</span></a></h1><p>前端Git版本库，分公共基础库与前端静态项目库两部分。</p><p class="tip"><strong>重要提示：禁止编辑所有项目目录下的<code>.gitlab-ci.yml</code>文件。</strong></p><h2 id="_1、公共基础库"><a href="#/git?id=_1%e3%80%81%e5%85%ac%e5%85%b1%e5%9f%ba%e7%a1%80%e5%ba%93" data-id="_1、公共基础库" class="anchor"><span>1、公共基础库</span></a></h2><p>该版本库，用于存放39各项目所引用的js、css等静态非图片项目文件。   </p><blockquote>
<p>Git项目地址：<a href="http://gitlab.39.net/static/common" target="_blank">http://gitlab.39.net/static/common</a></p></blockquote>
<h3 id="_11、本机关联git库"><a href="#" data-id="_11、本机关联git库" class="anchor"><span>1.1、本机关联Git库</span></a></h3><p><strong>一、自动创建common文件夹（此时Git会自动创建common文件夹并将最新代码更新到此文件夹下。）</strong>   </p><p>在项目的上级文件夹（如static文件夹）下执行以下命令：</p><pre v-pre="" data-lang="cmd"><code class="lang-cmd">git clone git@gitlab.39.net:static/common.git
cd common</code></pre>
