---


---

<h2 id="函数声明、调用、返回基础">函数声明、调用、返回基础</h2>
<p>Python中使用def关键字来声明函数，声明函数的格式为：</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">def</span>  <span class="token function">func_name</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">:</span> 
	 <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>body<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span> 
	 <span class="token punctuation">[</span><span class="token keyword">return</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">]</span>
</code></pre>
<p>有3个需要注意的地方：</p>
<ol>
<li>函数名后面必须加冒号</li>
<li>如果函数体和def不在同一行，则必须缩进</li>
<li>return指定函数返回值，用来结束函数
<ul>
<li>但return语句是可有可无的，如果不给return，则等价于加上了<code>return None</code>，即函数默认返回None结构</li>
</ul>
</li>
</ol>
<p>如果函数体body语句只有一行，或者可以简写为一行，则可以写在def的同行。例如：</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">def</span> <span class="token function">myfunc</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span>y<span class="token punctuation">,</span>z<span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token keyword">print</span><span class="token punctuation">(</span>x<span class="token operator">+</span>y<span class="token operator">+</span>z<span class="token punctuation">)</span>
</code></pre>
<p>函数声明好之后，就可以执行函数，执行函数也称为调用函数，方式为<code>func_name(args)</code>，例如：</p>
<pre class=" language-scss"><code class="prism  language-scss"><span class="token function">myfunc</span><span class="token punctuation">(</span><span class="token number">1</span>,<span class="token number">2</span>,<span class="token number">3</span><span class="token punctuation">)</span>
</code></pre>
<p>函数中往往会包含一个return或多个return语句，它可以出现在函数中的任意位置处，它用来结束函数的执行，并返回给定的值。例如：</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">def</span> <span class="token function">func</span><span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">:</span>
	<span class="token keyword">return</span> x<span class="token operator">+</span><span class="token number">5</span>
</code></pre>
<p>表示返回<code>x+5</code>的值，返回值是一种值类型，所以可以赋值给变量、可以输出、可以操作等等。例如：</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">print</span><span class="token punctuation">(</span>func<span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token comment"># 输出返回值 </span>

a<span class="token operator">=</span>func<span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">)</span> <span class="token comment"># 赋值给变量 </span>
<span class="token keyword">print</span><span class="token punctuation">(</span>a<span class="token punctuation">)</span> 

<span class="token keyword">print</span><span class="token punctuation">(</span>func<span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">)</span><span class="token operator">+</span><span class="token number">3</span><span class="token punctuation">)</span> <span class="token comment"># 数值操作</span>
</code></pre>
<p>return语句是可选的，如果函数中不指定return语句，则默认返回None，即类似于<code>return None</code>。</p>
<h2 id="关于函数参数">关于函数参数</h2>
<p>函数的参数其实也是变量，只不过这些变量是独属于函数的本地变量，函数外部无法访问。在函数调用的时候，会将给定的值传递给函数的参数，这实际上是变量赋值的过程。</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">def</span>  <span class="token function">myfunc</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span>y<span class="token punctuation">,</span>z<span class="token punctuation">)</span><span class="token punctuation">:</span> 
	 <span class="token keyword">print</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span>y<span class="token punctuation">,</span>z<span class="token punctuation">)</span> 

myfunc<span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">)</span>
</code></pre>
<p>def首先声明好函数，然后到了<code>myfunc(1,2,3)</code>时，表示调用函数(执行函数)，调用函数时会将给定的值<code>1,2,3</code>传递给函数的参数<code>x,y,z</code>，其实就是变量赋值<code>x=1,y=2,z=3</code>，然后使用print输出它们。</p>
<p>由于python是动态语言，无需先声明变量，也无需指定变量的类型，所以python的函数参数和返回值非常的灵活。任何类型的变量或数据结构都可以传递给参数，这实际上是变量赋值的过程。例如：</p>
<pre class=" language-python"><code class="prism  language-python">myfunc<span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">)</span> 
myfunc<span class="token punctuation">(</span><span class="token string">"abc"</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token string">"def"</span><span class="token punctuation">)</span> 
myfunc<span class="token punctuation">(</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">]</span><span class="token punctuation">,</span><span class="token number">4</span><span class="token punctuation">,</span><span class="token number">5</span><span class="token punctuation">)</span>
</code></pre>
<p>上面几个函数调用语句中，赋值给参数的值可以是数值类型，可以是字符串类型，可以是列表类型，也可以是其它任何数据类型。</p>
<h2 id="函数声明、调用的过程详述">函数声明、调用的过程详述</h2>
<p>def用来声明一个函数，python的函数包括函数名称、参数、函数体、函数体中涉及到的变量、返回值。</p>
<p>实际上，<strong>函数名称其实是一个变量名，def表示将保存在某块内存区域中的函数代码体赋值给函数名变量</strong>。例如：</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">def</span>  <span class="token function">myfunc</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span>y<span class="token punctuation">,</span>z<span class="token punctuation">)</span><span class="token punctuation">:</span> 
	 <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>CODE<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>
</code></pre>
<p>既然是变量，就可以进行输出：</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">def</span>  <span class="token function">myfunc</span><span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">:</span> 
	 <span class="token keyword">return</span> x<span class="token operator">+</span><span class="token number">5</span>  
	 
<span class="token keyword">print</span><span class="token punctuation">(</span>myfunc<span class="token punctuation">)</span>
</code></pre>
<p>输出结果：</p>
<pre class=" language-x86asm"><code class="prism  language-x86asm">&lt;function myfunc at 0x032EA6F0&gt;
</code></pre>
<p>由于python是解释型语言，所以必须先定义函数，才能调用函数。</p>
<p>如果导入一个模块文件，导入的时候会解释、执行文件中的代码，包括def语句，也就是说，导入文件时会先声明好函数。</p>
<h3 id="函数变量的细节">函数变量的细节</h3>
<p>请一定理解本节内容，也许细节方面可能会有些不准确，但对于深入理解函数来说(不仅限于python语言)，是非常有帮助的，特别是理解作用域规则的时候。</p>
<p>python是解释性语言，读一行解释一行，解释一行忘记一行。而函数是一种代码块，代码块是一个解释单元，是一个整体。<strong>在代码块范围内不会忘记读取过的行，也不会读一行就立即解释一行，而是读取完所有代码块内的行，然后统筹安排地进行解释</strong>。</p>
<p>当python读取到def所在行的时候，知道这是一个函数声明语句，它有一个属于自己的代码块范围，于是会读完整个代码块，然后解释这个代码块。在这个解释过程中，<strong>会记录好变量以及该变量的所属作用域(是全局范围内的变量还是函数的本地变量)，但一定注意，def声明函数的过程中不会进行变量的赋值(参数默认值除外，见下文)，只有在函数调用的时候才会进行变量赋值。换句话说，在def声明函数的过程中，在函数被调用之前，函数所记录的变量一直都是变量的地址，或者通俗一点理解为记录变量的名称，而不会进行变量的赋值替换</strong>。</p>
<p>实际上，变量的明确的值会当作常量被记录起来。如<code>a=10</code>的10被作为常量，而变量a赋值给变量b时<code>b=a</code>，a显然不会作为常量。</p>
<p>如下函数：</p>
<pre class=" language-python"><code class="prism  language-python">x<span class="token operator">=</span><span class="token number">3</span>  
<span class="token keyword">def</span>  <span class="token function">myfunc</span><span class="token punctuation">(</span>a<span class="token punctuation">,</span>b<span class="token punctuation">)</span><span class="token punctuation">:</span> 
	 c<span class="token operator">=</span><span class="token number">10</span>  
	 <span class="token keyword">print</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span>a<span class="token punctuation">,</span>b<span class="token punctuation">,</span>c<span class="token punctuation">)</span> 
	 
myfunc<span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">,</span><span class="token number">6</span><span class="token punctuation">)</span>
</code></pre>
<p>输出结果为：“3 5 6 10”。</p>
<p>上面的函数涉及到了4个变量：a、b、c、x。其中：</p>
<ul>
<li>全局变量x</li>
<li>本地变量a、b、c，其中本地变量a和b是函数的参数</li>
</ul>
<p>在def的过程中，会完完整整地记录好这些变量以及所属作用域，但只会记录，不会进行变量的赋值。</p>
<p>然后函数被调用，这时候才会开始根据记录的作用域搜索变量是否存在，是否已经赋值(非本地变量)，并对需要赋值的变量赋值：</p>
<ul>
<li>查找全局变量变量x，它在全局作用域内已经赋值过了，所以只需找到这个全局变量即可</li>
<li>查找本地变量a、b、c，它们是属于函数myfunc的本地变量，而a和b是参数变量，所以最先对它们进行赋值<code>a=5,b=6</code>，然后赋值普通的本地变量<code>c=10</code></li>
</ul>
<p>最后执行<code>print(x,a,b,c)</code>输出这些变量的值。</p>
<p>还需注意，python是读一行解释一行的，在函数调用过程中，因为<code>c=10</code>在<code>print()</code>的前面，所以是先赋值<code>c=10</code>，再执行print，如果print在<code>c=10</code>前面，则先执行print，再赋值，这显然是错误的，因为print()中使用了变量c，但目前还没有对其赋值。这和其它语言可能有些不同(特别是编译型语言)，它们可能会无视变量赋值以及变量使用的位置前后关系。</p>
<p>如果上面的示例中，函数myfunc调用之前，将变量x赋值为另一个值：</p>
<pre class=" language-python"><code class="prism  language-python">x<span class="token operator">=</span><span class="token number">3</span>  
<span class="token keyword">def</span>  <span class="token function">myfunc</span><span class="token punctuation">(</span>a<span class="token punctuation">,</span>b<span class="token punctuation">)</span><span class="token punctuation">:</span> 
	 c<span class="token operator">=</span><span class="token number">10</span>  
	 <span class="token keyword">print</span><span class="token punctuation">(</span>x<span class="token punctuation">,</span>a<span class="token punctuation">,</span>b<span class="token punctuation">,</span>c<span class="token punctuation">)</span> 
x<span class="token operator">=</span><span class="token number">33</span> 
myfunc<span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">,</span><span class="token number">6</span><span class="token punctuation">)</span>
</code></pre>
<p>这时将输出：“33 5 6 10”。因为x是全局变量，只有在函数调用的时候才会去找到变量x对应的值，而这时全局变量的值已经是33。</p>

