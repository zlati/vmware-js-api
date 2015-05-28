#Docs for VMware's vSphere web client JavaScript API
VMware started supporting HTML in their vSphere web client in 2014. They also introduced a JS API to help developers build services on top of their web client.

###Notes
Define *ns* as shortcut for your app's namespace - *var ns = com_mycompany_myapp;*

###Global  
- *WEB_PLATFORM.getObjectId();*  
Get the current object ID. 

###Dialogs
- *WEB_PLATFORM.setDialogTitle('My title');*   
Change dialog title at runtime.  

- *WEB_PLATFORM.closeDialog();*  
Close the current modal dialog.  

###Resources
- *ns.getString('myvariable');*   
Load a variable from the current language **.properties** file in **/locale**   

###Other
- *window.location.href = "/vsphere-client/MYCOMPANY/resources/myView.html" + document.location.search;*  
Not a part from vSphere but still a useful one. Redirect within a modal dialog without closing it and inclose the query string. Do not forget to use *WEB_PLATFORM.setDialogTitle('My title');* in the new view so you don't end up with the same dialog name.

- *icon16=Embed("../../webapp/assets/img/icon16.png")*
Embed image in the */locale* resources files. After that you can use this in your *plugin.xml* file:  
``<root>``  
 `` <actionUrl>/vsphere-client/compuverde/resources/clusterCreateFilesystemWizard.html</actionUrl>``  
 `` <dialogTitle>#{clusterCreateFilesystemWizard.title}</dialogTitle>``  
 `` <dialogSize>720,580</dialogSize>``  
 `` <dialogIcon>#{compuverde.html.icon16}</dialogIcon>``  
 ``</root>``  

