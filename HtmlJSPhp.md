<h1>Basic guide to help me keep in touch with HTML, Javascript and Php!</h1>

<h3>Starting with how to use Google developer tools: </h3>
<h4> <li> Console -> </li> </h4><br></li> 
<li>Add any log in JS to help in debugging, debug, info, warn, error etc. <b>console.info("Reached here!").</b> Click on the error message to navigate to the source. Grouping and formatting is possible by using <b> console.group("%cFirst Step","font-size: x-large") <br> console.log("%i + %i = %s",2,2,"4"); <br> console.groupEnd(); </b> <br> 
%c -> css, %i -> integer, %s -> string <br> </li>
<li> Add assert statements as <b>console.assert(expression)</b> to check if expected value came in place or not. <br> </li>
<li>Use <b> clear() </b> to clear the console screen. <br></li>
<li> <b>console.dir(objectName) </b> -> To have Javascript annotation. <br></li>
<li> <b>console.time("label1"); &nbsp console.timeEnd("label1"); </b> <br></li>
<li> <b> debugger; </b>  -> adds the breakpoint when this javascript executes. </li>
<li> You can check the value of the dom element from console </li>
<li> Can call the html element directly -> <b> $('idOfRequiredThing') </b> <br> It can be used along with inspect($('id')) and it will change the console to source and select the records in page. <br></li>
<li> Monitor events -> <b> monitorEvents($('id'), "mouse") </b> </li>
