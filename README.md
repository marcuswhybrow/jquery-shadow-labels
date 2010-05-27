Shadow Labels
=============

Shadow Labels is a jQuery plugin which combines form labels and inputs for a streamlined experience. I call it a shadow label because it's value now lives inside of its counterpart input element displayed when needed. But when the input gains focus disappears instantly.

The form does not require any out of the ordinary attributes or divs, so if JavaScript is disabled you degrade gracefully.

Usage
=====

Link to jQuery
--------------

Ensure that you have included jQuery in your document:

    <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.4/jquery.min.js"></script>

Link to the Plugin
------------------

Include the plugin file itself:

    <script type="text/javascript" src="jquery.shadowlabels.js"></script>

Call the plugin
---------------

Here I am calling the plugin from within the standard jQuery ready function, on all form elements within the page:

    $(function() {
        $('form').shadowLabels(); 
    });

Plugin Options
--------------

The plugin accepts the following options:

    $('form').shadowLabels({
        text: true,
        textarea: true,
        showValues: false,
    });

### text

Apply the plugin to input elements where type="text" within the matched form elements (true by default).

### textarea

Apply the plugin to textarea elements within the matched form elements (true by default).

### showValues

If a field has a value (i.e. the default value displayed) it can be shown in brackets after the label by settings showValues to true.

However is seems Firefox likes to remember form field values over page refreshes, meaning that the label after a refresh becomes the previous label plus the previous default value, which then becomes the new default value, which gets incorporated into the next page refresh. Suffice to say, this is not a desired effect, and until rectified showValues should be left false.