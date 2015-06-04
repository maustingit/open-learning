$('#Opt-inY').is(':checked');

If it is checked, then true is returned - if it is not, then false is returned.

So if I have two Opt-in questions - Opt in Newsletter and a main "Opt-in" question, and I want to check the main Opt-in if the supporter is subscribed to the newsletter Opt-in when the page loads, a few lines in a script in the footer would do: 

if ($('#Opt-in_newsletterY').is(':checked')) {
  $( "#Opt-inY" ).prop( "checked", true );
}

This will check the Opt-in question if the Opt-in is checked. You can also add "events" that trigger when something changes, so for example, as above - to make this happens when the Opt-in newsletter question is checked:

$('#Opt-in_newsletterY').click(function() {
  if ($(this).is(':checked')) {
  $( "#Opt-inY" ).prop( "checked", true );
  }
});
