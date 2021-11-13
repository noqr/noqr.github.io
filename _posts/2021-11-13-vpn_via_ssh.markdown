---
layout: post
title:  "Технологическое: VPN своими руками при помощи ssh"
date:   2021-11-13 09:01:00 -0700
categories: vpn ssh technology
---

В условиях, когда идет массовое ограничение доступа к информационным ресурсам, 
можно обойтись без всяких VPN, если у вас есть `ssh` доступ
к любому серверу за рубежом. Используем тот факт, ssh имеет встроенный `SOCKS 5` прокси.

Соединяемся 
`ssh -D 4711 someserver.com`

Можно запустить в фоновом режиме
`ssh -fTND 4711 someserver.com`

Далее меняем сетевые настройки (Linux)

![socks5_proxy.png](/assets/socks5_proxy.png)

Проверям свой IP адрес браузером, например, здесь `https://eax.me/ip/`. Или просто идем на [rutracker.org](https://rutracker.org/)