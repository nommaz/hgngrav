---
title: İletişim
addresses:
    -
        title: 'SATIŞ ve PAZARLAMA'
        address_1: 'Buyaka Kule 3 Kat:11 No:68'
        address_2: '<b>Ümraniye</b> - Istanbul 34760'
        phone_1: '444 5 446 / 444 5 HGN'
        phone_2: '+90 (216) 510 06 27'
        email: pazarlama@hugin.com.tr
        image: harita_satis.jpg
        url: 'https://goo.gl/maps/cZq9fruauFz'
    -
        title: 'MERKEZ SERVİS'
        address_1: 'Subaşı mh. Yurdagül sk. No:28'
        address_2: '<b>Çatalca</b> - Istanbul 34540'
        phone_1: '0850 252-5272'
        phone_2: '+90 (212) 795-0528'
        email: merkezservis@hugin.com.tr
        image: harita_catalca.png
        url: 'https://goo.gl/maps/vjgLiVyqc5u'
    -
        title: 'MUHASEBE ve ARGE'
        address_1: 'Meclis-i Mebusan Caddesi 77/3'
        address_2: '<b>Fındıklı</b> - Istanbul 34427'
        phone_1: '+90 (212) 251-7343'
        phone_2: '+90 (212) 251-7348'
        email: huginfo@hugin.com.tr
        image: harita.jpg
        url: 'https://goo.gl/maps/oFCr3EYVXQM2'
form:
    name: contact
    fields:
        -
            name: name
            label: İsim
            placeholder: 'İsminizi girin'
            autocomplete: 'on'
            type: text
            classes: twelve
            validate:
                required: true
        -
            name: email
            label: Eposta
            placeholder: 'Eposta adresinizi girin'
            type: email
            classes: twelve
            validate:
                required: true
        -
            name: subject
            label: Konu
            placeholder: Konu
            autocomplete: 'on'
            type: text
            classes: twelve
            validate:
                required: true
        -
            name: detail
            label: Detay
            placeholder: Detay
            type: textarea
            classes: twelve
            validate:
                required: true
        -
            name: g-recaptcha-response
            label: Captcha
            type: captcha
            recaptcha_site_key: 6LdgbRYUAAAAAPhaFm7ntuwOeFStDVBAjstguTpy
            recaptcha_not_validated: 'Captcha geçersiz!'
            validate:
                required: true
    buttons:
        -
            type: submit
            value: Submit
        -
            type: reset
            value: Reset
    process:
        -
            captcha:
                recaptcha_secret: 6LdgbRYUAAAAADZHPRZQJibswQbDR2t_2Ac7HcvC
        -
            email:
                subject: '[Site Contact Form] {{ form.value.name|e }}'
                body: '{% include ''forms/data.html.twig'' %}'
        -
            save:
                fileprefix: contact-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            message: 'Thank you for getting in touch!'
        -
            reset: true
---

## İletişim
Aşağıdaki formu doldurarak veya bu sayfadaki email ve telefon numaralarımız vasıtası ile bizle iletişime geçebilirsiniz.  
*Ürününüz ile ilgili destek veya bilgi talepleriniz için sitemizin [destek](/support) bölümünden de faydalanabilirsiniz.*