# hashcatJS
An implementation of the hashcat rules engine in javascript

##For registration pages
HashcatJS can be used for client side verification of password registrations. It has the ability to spot if a user's password falls into the top 10,000 picked passwords, and it also has the ability to see if those passwords fall into rule sets. More information on rule based password cracking can be found [here](https://www.praetorian.com/blog/statistics-will-crack-your-password-mask-structure)

An example of registration can be found here 

##For brute forcing login pages
HashcatJS can also be used to brute force a login page. Given a page with no account lockout, HashcatJS can be used to send requests to the server for common passwords and rule variations of those common passwords

##Example code

To use this library, simply include the rule set you want, the dictionary you want to use, and the hashcatJS engine

```html
		<script src="rule.js"></script>
		<script src="passwords.js"></script>
		<script src="hashcatJS.js"></script>
		<script>
		    checkThisPassword(usersPassword, 9999) //tweak 9999 to alter the number of dictionary entries to try, max size 9999 with default dictionary
		</script>
```

###Rule Set
The rule sets must be of the following form

```javascript
    var ruleSet = ":\nr\nT0\nu\n]\nd"
    
```


More information on rules can be found [here](https://hashcat.net/wiki/doku.php?id=rule_based_attack)

###Dictionary
The dictionary must be of the following form

```javascript
    var passwords = ["password", "123456", "12345678", "1234"
```
