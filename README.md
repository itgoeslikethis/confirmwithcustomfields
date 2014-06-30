confirmwithcustomfields
=======================
Barebones proof of concept for transferring custom field values from list to list via an email click.

The way this is used:
1. Modify the index.html so it works with your target form code.
2. That means you might need to add javascript to handle other types of form value
3. Setup a campaign that links to: http://yoursite.com/location/of/script/?name=[fullname]&email=[email]&interests=[interests]
4. This will therefore be working with a normal list with an additional custom field called "interests"
5. When the recipient clicks on the link it directs them to the above but replaces all the personalisation parameters in the querystring with their actual data
6. The javascript in index.html looks at the query string parameters and populates the form, including checking all relevant boxes in the Interests section.
7. Having done that the javascript then submits the form, thus transferring the customer's information to the new list

There's a bunch of things that are hardcoded in this example that would need to be modified or generalised or improved

1. The form code points to a form on my campaign monitor account
2. The javascript uses the labels which belong to my form
3. The design is clunky (ie it shows the form before it submits)

All this is achievable, but this is a *proof of concept*, it's not intended to be dropped into production.
