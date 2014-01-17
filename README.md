SPClientPeoplePickerPlugin
==========================

This is a jQuery plugin for enabling People Picker control on SharePoint 2013 pages.

1. Download the script files and upload it to a location (either in style library) or 15 hive on your SharePoint server
2. Provide a reference to the jQuery library before we use the plugin
3. Provide a reference to the sppeoplepicker.min,js on the page
4. Create a div element with an id attribute
5. call the spPeoplePicker() on the div element in document.ready function

I also uploaded the original JS file. It is open and you can change it as per your requirement. 

=================================================================================================

Sample Code

=================================================================================================

<script src="../Style Library/jquery.min.js"></script>
<script src="../Style Library/SPPeoplePicker.js"></script>
<script type="text/javascript">
	$(document).ready(function () {
				$("#peoplePickerDiv").spPeoplePicker();
				$("#anotherPeoplePickerDiv").spPeoplePicker();

			
			$("#pp1").click(function(){
				alert($("#peoplePickerDiv").getUserInfo());
				return false;
			});
    		$("#pp2").click(function(){
				alert($("#anotherPeoplePickerDiv").getUserInfo());
				return false;
			});

	});
	
</script>
<table class="spPeoplePickerTable" width="50%" cellpadding="10" cellspacing="1">
	<tr>
		<td>People Picker 1: </td>
		<td><div id="peoplePickerDiv"></div></td>
		<td><button id="pp1">Show</button></td>
	</tr>
	<tr>
		<td>People Picker 2:</td>
		<td><div id="anotherPeoplePickerDiv"></div></td>
		<td><button id="pp2">Show</button></td>
	</tr>

</table>

==============================================================================================
