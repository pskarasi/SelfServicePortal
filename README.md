<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Osttra Support</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 20px;
        }
        form {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input, select, textarea {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        textarea {
            height: 120px;
        }
        input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #45a049;
        }
        h2 {
            text-align: center;
        }
    </style>
</head>
<body>

    <h2>Contact Osttra Support</h2>

    <form action="https://osttra--osttrapoc.sandbox.my.salesforce.com/servlet/servlet.WebToCase?encoding=UTF-8&orgId=00DAe000005qfnN" method="POST">

        <input type="hidden" name="orgid" value="00DAe000005qfnN">
        <input type="hidden" name="retURL" value="http://osttra.com">
        <input type="hidden" name="external" value="1">
        <input type="hidden" name="00NNz00000B5c7V" value="https:sampleosttra.com/generatecasses">


        <label for="recordType">Case Record Type:</label>
        <select id="recordType" name="recordType">
            <option value="012Nz000003siry">Customer Care Case</option>
        </select><br>

        <label for="name">Contact Name:</label>
        <input type="text" id="name" maxlength="80" name="name" required><br>

        <label for="email">Email:</label>
        <input type="email" id="email" maxlength="80" name="email" required><br>

        <label for="subject">Subject:</label>
        <input type="text" id="subject" maxlength="80" name="subject" required><br>

        <label for="description">Description:</label>
        <textarea id="description" name="description" required></textarea><br>

        <label for="servicePlatform">Service Platform:</label>
        <select id="servicePlatform" name="00NNz00000B5c58" title="Service Platform">
            <option value="">--None--</option>
            <option value="MarkitServ">MarkitServ</option>
            <option value="Traiana">Traiana</option>
            <option value="TriOptima">TriOptima</option>
        </select><br>

        <label for="environment">Environment:</label>
        <select id="environment" name="00NNz00000B5c4z" title="Environment">
            <option value="">--None--</option>
            <option value="Internal">Internal</option>
            <option value="N/A (Not Applicable)">N/A (Not Applicable)</option>
            <option value="Production">Production</option>
            <option value="UAT (User Acceptance Testing)">UAT (User Acceptance Testing)</option>
        </select><br>

        <label for="priority">Priority:</label>
        <select id="priority" name="priority">
            <option value="Regular">Regular</option>
            <option value="Time Sensitive">Time Sensitive</option>
        </select><br>


        <input type="submit" value="Submit">

    </form>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DAe000005qfnN',
				'OSTTRA_Messaging_Service',
				'https://osttra--osttrapoc.sandbox.my.site.com/ESWOSTTRAMessagingServi1740843154697',
				{
					scrt2URL: 'https://osttra--osttrapoc.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://osttra--osttrapoc.sandbox.my.site.com/ESWOSTTRAMessagingServi1740843154697/assets/js/bootstrap.min.js' '></script>
<button id=""launchChatButton" onclick="launchChat()">
       Chat With Our Agents!
</button>

<script>
    function launchChat(){
	 SessionStorage.SetItem( 'messagingStartCheck','Yes');
	initEmbeddedMessaging();
	console.log('loading messaging now');
		setTimeout(() => {
       embeddedservice_bootstrap.utilAPI.launchChat()
	                .then (() => {
					console.log('Inside Launch Chat');
					}).catch(() => {
					console.log('Inside Launch Chat Catch Block');
					}).finally (() => {
					console.log('Inside Launch Chat finally Block');
					});
            },2000);
			}
</script>
</body>
</html>			

