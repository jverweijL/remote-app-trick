# Liferay React Configuration Trick
This repo will show you a trick.
Normally you can configure a webcomponent/client extension with properties.
For technical administrators this can be fine, but for page/content editors this can be a bit confusing.
How should they know what properties are available? What should the format look like?
To overcome this you can also do the following: use a fragment with a webcomponent.
Fragments can have configuration options and you can use these configuration options to configure the webcomponent including hints/tips and/or dropdown selectors.
Downside is that administrators need to make sure the js is actually activated on global/site/page level upfront.

The fragment I'm using for this example looks like this:
```
<div class="fragment_101">
	<lfr-test config01="${configuration.config01}" p1="${configuration.p1}">
		<data>
			currently not used by the remote app but you could also embed the data in a tag and query the dom for the actual data
			{config01: ${configuration.config01},
			 p1: ${configuration.p1}
			}</data>
	</lfr-test>
</div>
```