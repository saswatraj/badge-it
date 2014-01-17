# BADGE-IT  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![](http://blog.texasswede.com/wp-content/uploads/2013/08/github_small.png "Badge-IT")

Create your css customized badges to display your github profile on websites using html,css and this javascript plugin.Uses jquery version 2 and has been tested to be compatible with all browsers : firefox,chrome and IE.__No authentication required__. Only github username required to fetch the stats. Please see the example file and code below for more details.

## STEPS 
### Include the javascript files
```html
<head>
<title>Example</html>
<script src="jquery.js"/>
<script src="githubapi.js"/>
</head>
```
Include the javascript files and the jquery library into your page in the head section

### Create the structure
Create the html structure and design it according to your design specifications.__Give specific id's to the containers you want to display stats or set hyperlinks to github urls of the profile__.In the example the `div` with `id` 'git-button' is the div designed to be the badge.

### Initialize the plugin to fetch stats
Call the show fucntion of the WidGit. Pass the id of the container along with the stat number to show the stat there.If it is a url you want to hyperlink to then send the id of `<a>` tag and it plugin will set the href attribute to that url.

```javascript
WidGit.show(
	'profile_name',
	[{id:'container1',stat:<stat_number>},{id:'container2',stat:<stat_number>}]
	);
```

The stats are numbered accordingly.See the list below for the stat number mappings.The attribute column specifies the attribute of the container that will be replaced.

Stat Number | Corresponding Github Property | Attribute
--- | ------- | -----
0 | login_name | innerHTML
1 | user_id | innerHTML
2 | avatar_url | src
3 | gravatar_id | innerHTML
4 | user url | href
5 | followers url | href
6 | following url | href
7 | gists url | href
8 | subscription url | href
9 | organization url | href
10 | repositories link | href
11 | user type | innerHTML
12 | total repos | innerHTML
13 | total forks | innerHTML
14 | followers | innerHTML
15 | following | innerHTML

For any other stat number the inner html will be replaced by `undefined`.

## Bugs 
If you find any bugs please mail to me at : __saswatrj2010@gmail.com__

