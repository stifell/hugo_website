---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Контакты
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

  # Contact details (edit or remove options as required)
  email: matyushkin_d@list.ru
  phone: +7 (976) 475-##-##
  address:
    street: 21 building 1, Miklukho-Maklai street
    city: Moscow
    region: Russian Federation
    postcode: '117198'
    country: Russian Federation
    country_code: RU
  coordinates:
    latitude: '55.65176'
    longitude: '37.508274'
  directions: Go into the building, then yourself, but I'm not waiting for you!
  office_hours:
    - 'Monday 10:00 to 13:00'
    - 'Wednesday 09:00 to 10:00'
  contact_links:
    - icon: vk
      icon_pack: fab
      name: VK Me
      link: 'https://vk.com/extra_858'

design:
  columns: '2'
---
