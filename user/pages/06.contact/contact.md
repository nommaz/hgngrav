---
title: Contact
menu: Contact

heading: this is heading
sub_heading: sub_heading is here

showcase_image: hero-image.png

buttons:
    - text: Free Trial
      url: '#'
      class: button trial animated shake
    - text: Learn More
      url: '#'
      class: button learn-more smoothscroll

addresses:
    - title:
      address_1: Meclis-i Mebusan Caddesi 77/3 34427
      address_2: Fındıklı - Istanbul / TÜRKİYE
      phone_1: +90 (212) 251 73 43
      phone_2: +90 (212) 251 73 48
      email: huginfo@hugin.com.tr
      image: harita.jpg
      url: http://goo.gl/maps/uE12k
    - title: SATIŞ ve PAZARLAMA
      address_1: Buyaka Kule 3 Kat:11 No:68
      address_2: Ümraniye - Istanbul / TÜRKİYE
      phone_1: 444 5 446 / 444 5 HGN
      phone_2: +90 (216) 510 06 27
      email:
      image: harita_satis.jpg
      url: https://www.google.com/maps/place/Buyaka/@41.0269949,29.1286602,17z/data=!4m2!3m1!1s0x0:0x726fb77d4e9c67c5?hl=tr-TR
    - title: FABRİKA
      address_1: Subaşı mh. Yurdagül sk. No:28
      address_2: Çatalca - Istanbul / TÜRKİYE
      phone_1: +90 (212) 795 05 28
      phone_2:
      email:
      image:
      url:

form:
    name: contact

    fields:
        - name: name
          label: Name
          placeholder: Enter your name
          autocomplete: on
          type: text
          classes: twelve
          validate:
            required: true

        - name: email
          label: Email
          placeholder: Enter your email address
          type: email
          classes: twelve
          validate:
            required: true

        - name: subject 
          label: Subject
          placeholder: Enter subject
          autocomplete: on
          type: text
          classes: twelve
          validate:
            required: true

        - name: detail
          label: Detail
          placeholder: Enter your message
          type: textarea
          classes: twelve
          validate:
            required: true

        - name: g-recaptcha-response
          label: Captcha
          type: captcha
          recaptcha_site_key: 6LdgbRYUAAAAAPhaFm7ntuwOeFStDVBAjstguTpy
          recaptcha_not_validated: 'Captcha not valid!'
          validate:
            required: true

    buttons:
        - type: submit
          value: Submit
        - type: reset
          value: Reset

    process:
        - captcha:
            recaptcha_secret: 6LdgbRYUAAAAADZHPRZQJibswQbDR2t_2Ac7HcvC
        - email:
            subject: "[Site Contact Form] {{ form.value.name|e }}"
            body: "{% include 'forms/data.html.twig' %}"
        - save:
            fileprefix: contact-
            dateformat: Ymd-His-u
            extension: txt
            body: "{% include 'forms/data.txt.twig' %}"
        - message: Thank you for getting in touch!
        - reset: true
---

# Contact Us
Please fill in this form and submit to us

