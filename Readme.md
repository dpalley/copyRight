# jQuery.CopyRight.js

We have all seen them - professional-looking websites with copyright notices that are several years out of date. A small oversight can make an otherwise stellar website into something that doesn't look quite as stellar. This is a jQuery plugin that will automatically keep those copyright notices up to date.

The steps to implement this are pretty simple.

1). You hard-code this year's value into an HTML element as part of your copyright notice. If you are modifying an existing site, put the earliest year for which you want the copyright notice to cover. This needs to be a standard 4-digit value. The example code shows a span element with *id="year"*. If you choose, you may leave this element blank.
    '<p>Copyright <span id="year">2014</span><p>'
(optionally)
    '<p>Copyright <span id="year"></span><p>'

2). Add the function call to your JavaScript code that examines the element that you specified in step 1.
    '$("#year").copyRight();'

3). Link to the jQuery file from your html file.
    '<script src="/js/jquery.copyRight.js"></script>'

Here is a  brief overview of the code.
The function reads the contents from the HTML element (see step 1) into a string variable. If the contents of the HTML element is anything other than a 4-digit number, the function overwrites the contents with the current year.

The function also retrieves the current year from the 'Date' value of the user's computer and stores it into a numeric variable. If the contents of the HTML element is a 4-digit number, the function compares the two values. If the two values are not equal (uses !=, not !==), the function modifies the string content of the HTML element to include the 'firstYear' and 'thisYear' values. If the two values are equal(uses ==, not ===), the function doesn't change the HTML element.
