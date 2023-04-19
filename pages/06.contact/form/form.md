---
title: 'Contact Form'
form:
    name: contact-form
    fields:
        -
            name: name
            label: Name
            classes: form-control
            placeholder: 'Enter your name'
            autofocus: 'on'
            autocomplete: 'on'
            type: text
            position: left
            validate:
                required: true
        -
            name: email
            label: Email
            classes: form-control
            placeholder: 'Enter your email address'
            type: email
            position: left
            validate:
                required: true
        -
            name: message
            label: Message
            placeholder: 'Enter your message'
            type: textarea
            classes: form-control
            position: right
            validate:
                required: true
    buttons:
        -
            type: submit
            classes: button
            value: Submit
    process:
        -
            email:
                subject: '[Site Contact] {{ form.value.name|e }}'
                body: '{% include ''forms/data.html.twig'' %}'
published: false
---

# Contact form

Some sample page content