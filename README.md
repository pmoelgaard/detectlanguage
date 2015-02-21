DetectLanguage JavaScript API
===

Small convenience library allowing developers to easily interact with the DetectLanguage Service API.

Offical Website:
[https://detectlanguage.com/](https://detectlanguage.com/)


---

Sample Usage:

    var DetectLanguage = require('../index');
    var detectLanguage = new DetectLanguage({
        key: '[INSERT YOUR KEY HERE]'
    });
    
    var dataSimple = "I love Titanic.";
    detectLanguage.detect(dataSimple, function(error, result) {
        console.log(JSON.stringify(result));
    });
    
    var dataBulk = [
        "I love Titanic.",
        "I hate Titanic.",
        "I like Titanic."
    ]
    detectLanguage.detect(dataBulk, function(error, result) {
        console.log(JSON.stringify(result));
    });
    
    detectLanguage.languages(function(error, result) {
        console.log(JSON.stringify(result));
    });
    
    detectLanguage.status(function(error, result) {
        console.log(JSON.stringify(result));
    });

