### Element ####

Element is a very rudimentary Backbone like view layer. It allows the user to create a view, define events and perform actions on that view.
Element relies on vanilla javascript to interact with the dom.

example:

var element = require('./element');

var hello = element({

    events: {
        'click .hello': 'hello'
    }

    initialize: function () {
        this.render();
    }

    makeHello: function () {
        var hello = document.createElement('div');
        this.el.appendChild(hello);
    }

    render: function () {
        this.makeHello();
    }

    hello: function (e) {
        e.target.innerText = 'hello';
    }

});


new Hello({el: document.getElementsByTagName('body')})