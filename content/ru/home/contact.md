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
    street: ул. Миклухо-Маклая, 21 к. 1
    city: г. Москва
    region: Российская Федерация
    postcode: '117198'
    country: Российская Федерация
    country_code: RU
  coordinates:
    latitude: '55.65176'
    longitude: '37.508274'
  directions: Зайдите в здание, а дальше сами, но я вас не жду!
  office_hours:
    - 'Понедельник 10:00-13:00'
    - 'Среда 09:00-10:00'
  contact_links:
    - icon: vk
      icon_pack: fab
      name: Мой VK
      link: 'https://vk.com/extra_858'

design:
  columns: '2'
---
