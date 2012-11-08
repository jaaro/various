<?xml version="1.0" encoding="UTF-8"?><Module xmlns:os="http://ns.opensocial.org/2008/markup">
<ModulePrefs title="Pogoda"
               title_url="@export-moduleprefs-title-url@"
               screenshot="@export-moduleprefs-screenshot@"
               thumbnail="@export-moduleprefs-thumbnail@"
               description="Pogoda"
               author="Love"
               author_email="webmaster@loveapp.eu"
               height="@export-moduleprefs-height@"
               width="@export-moduleprefs-width@">
<Require feature="opensocial-0.9" />
<Require feature="views" />
<Require feature="nk" />

</ModulePrefs>

 <Content type="html" view="home.right"><![CDATA[
  <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
 "http://www.w3.org/TR/html4/loose.dtd">
 <div id="content">
	<div class="main_column_right">
    <div class="weather_box" style="width: 100%; height: 96px;">
	<div class="weather_box_content">
     <div class="weather_box_inner">
        
        <div class="weather_loading">
			<div>
				<img src="http://static.pogoda-nk.pl/images/weather/loading.gif?42407b" />
			</div>
            ładowanie prognozy pogody...
        </div>
		
     </div>
	 </div>
    </div>
	</div> 
 </div>
   <script type="text/javascript" src="http://code.jquery.com/jquery-1.7.1.min.js"></script>
   <script type="text/javascript" src="http://pogoda-nk.pl/nkframe/js/nkframe.php?3fb1e9"></script>
   	<script type="text/javascript" src="http://static.pogoda-nk.pl/scripts/common.js?60f633"></script>
   	<link rel="stylesheet" href="http://static.pogoda-nk.pl/css/style.css?540cde"></script>
      
   <script type="text/javascript">
    gadgets.util.registerOnLoadHandler(function() {
		 var params = {};

		params[gadgets.io.RequestParameters.AUTHORIZATION] = gadgets.io.AuthorizationType.SIGNED;
		params[gadgets.io.RequestParameters.REFRESH_INTERVAL] = 0;
		params[gadgets.io.RequestParameters.METHOD] = gadgets.io.MethodType.POST;
		params[gadgets.io.RequestParameters.POST_DATA] = gadgets.io.encodeValues({st:shindig.auth.getSecurityToken()});

		gadgets.io.makeRequest('http://pogoda-nk.pl', function(data) {
			$('#content').html(data.data);
		},params);
    });
   </script>
]]></Content>

<Content type="html" view="canvas"><![CDATA[
  <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
 "http://www.w3.org/TR/html4/loose.dtd">
 <div id="content">
	        <div class="weather_loading" style="position:relative;top:40px;">
			<div>
				<img src="http://static.pogoda-nk.pl/images/weather/loading.gif?42407b" />
			</div>
            ładowanie prognozy pogody...
        </div>
		
 </div>
   <script type="text/javascript" src="http://code.jquery.com/jquery-1.7.1.min.js"></script>
   <script type="text/javascript" src="http://pogoda-nk.pl/nkframe/js/nkframe.php?3fb1e9"></script>
   	<script type="text/javascript" src="http://static.pogoda-nk.pl/scripts/common.js?60f633"></script>
   	<link rel="stylesheet" href="http://static.pogoda-nk.pl/css/style.css?540cde"></script>
      
   <script type="text/javascript">
    gadgets.util.registerOnLoadHandler(function() {
		 var params = {};

		params[gadgets.io.RequestParameters.AUTHORIZATION] = gadgets.io.AuthorizationType.SIGNED;
		params[gadgets.io.RequestParameters.REFRESH_INTERVAL] = 0;
		params[gadgets.io.RequestParameters.METHOD] = gadgets.io.MethodType.POST;
		params[gadgets.io.RequestParameters.POST_DATA] = gadgets.io.encodeValues({st:shindig.auth.getSecurityToken()});
		
		var url = ''; $.each(gadgets.views.getParams(), function(k) { url += k;});
		if($.trim(url) == '' || url.substring(0,1)!='/') url ='/box';
		
		gadgets.io.makeRequest('http://pogoda-nk.pl'+url, function(data) {
			$('#content').html(data.data);
		},params);
    });
   </script>
]]></Content>

</Module>