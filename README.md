# markx

### markdown + syntax highlighting => html

Markx is a command line tool for node.js to convert markdown and code blocks into html.  It also has the ability to preview your markdown files live with auto refresh.

##Install

	npm install -g markx

##Usage

	Usage: markx [file]

	Options:

		-h, --help            output usage information
		-V, --version         output the version number
		-l, --lang <lang>     Language for syntax highlighting (default: auto)
		-n, --nohl            Disable syntax highlighting
		-p, --preview <port>  Start a server to get a live preview

	Examples:

		# convert markdown and code blocks to html
		$ markx blog.md > blog.html

		# convert markdown and specific language code blocks to html
		$ markx --lang javascript blog.md > blog.html

		# live preview of your markdown file
		$ markx --lang javascript --preview 8001 blog.md

##Example

###Markdown
<pre>
#This is a heading

This is a paragraph

	var a = '123';
	var f = function() {
		return 4;
	}
</pre>

###Output
<pre>
&lt;h1&gt;This is a heading&lt;/h1&gt;
&lt;p&gt;This is a paragraph&lt;/p&gt;
&lt;pre&gt;&lt;code&gt;&lt;span class="keyword"&gt;var&lt;/span&gt; a = &lt;span class="string"&gt;'123'&lt;/span&gt;;
&lt;span class="keyword"&gt;var&lt;/span&gt; f = &lt;span class="function"&gt;&lt;span class="keyword"&gt;function&lt;/span&gt;&lt;span class="params"&gt;()&lt;/span&gt; {&lt;/span&gt;
&lt;span class="keyword"&gt;return&lt;/span&gt; &lt;span class="number"&gt;4&lt;/span&gt;;
</pre>

##Live Preview
	
The `--preview` option lets you preview your markdown files before generating them as html.  When you open your browser to your live preview, you don't have to bother with refreshing every time you make a change to your markdown file, markx will automatically refresh your browser when it detects a change.  How cool is that?

##CSS for Syntax Highlighter

[Here](https://github.com/jgallen23/highlight.js/tree/master/src/styles) are some css files that will style the code blocks. 

##Support Languages

[Here](https://github.com/jgallen23/highlight.js/tree/master/src/languages) are the supported languages for syntax highlighting.

##Future
- pass in custom header and footer
- different themes for live preview
