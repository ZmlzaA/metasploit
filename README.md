# metasploit

![metasploit](https://itsecforu.ru/wp-content/uploads/2019/02/metasploit-fedora.jpg)


```
Документация:

https://ptestmethod.readthedocs.io/en/latest/LFF-IPS-P4-PostExploitation.html
https://www.infosecmatter.com/list-of-metasploit-windows-exploits-detailed-spreadsheet/
```

````
run post/windows/gather/enum_devices — получить список установленных устройств;
run post/multi/gather/check_malware проверить файл на VIRUS TOTAL’е;
run post/windows/gather/enum_dirperms найти привилегированные пути в Windows;
run post/windows/gather/enum_domain – перечислить все доступные домены в Active Directory;
run post/multi/gather/dns_bruteforce – хотим побрутить домен используя чужие ресурсы? Ноу проблемо эта опция для вас;
run post/multi/gather/dns_reverse_lookup — Вы станете днс сервером для Вашего клиента. Соотсветственно можно манипулировать службами DNS;
run post/windows/gather/enum_domain_tokens — Воруем токены авторизованных пользователей в Windows;
run post/multi/gather/enum_vbox — чекаем на наличие Virtual Box машины;
run post/windows/gather/enum_domains – получить список доменов;
run post/multi/gather/env – получить переменные окружения полезно так же при эскалациях;
run post/multi/gather/filezilla_client_cred – Из моих любимых выдернуть пароли из файлзиллы;
run post/windows/gather/enum_files – собирает различные конфиги и дат файлы полезная опция при ресерче жертвы;
run post/multi/gather/find_vmx – получить список всех виртуальных машин;
run post/windows/gather/enum_hostfile читаем hosts файл;
run post/multi/gather/firefox_creds крадем пароли из firefox;
run post/windows/gather/enum_ie – так же для ie;
run post/windows/gather/enum_ms_product_keys – Воруем ключики лицензий;
run post/multi/gather/ping_sweep – пингуем хосты;
run post/windows/gather/enum_powershell_env – получить переменные окружения powershell;
run post/multi/gather/run_console_rc_file – запустить в консоли rc файл;
run post/windows/gather/enum_proxy – чекаем на прокси сервер (актуально чаще для организаций);
run post/multi/gather/skype_enum – Получить СКАЙП ПАРОЛИ;
run post/windows/gather/enum_putty_saved_sessions – получаем сессии в PUTTY (SSH);
run post/multi/gather/thunderbird_creds – получить пароли с почтового клиента;
run post/windows/gather/enum_services – получить список сервисов запущенных на машине. Удобно отследить сервисы;
run post/multi/gather/wlan_geolocate – узнать локацию интерфейса wlan;
run post/windows/gather/enum_shares – получить список общих дисков;
run post/multi/general/close – закрыть сессию метерпретер;
run post/windows/gather/enum_snmp – чекаем на snmp;
run post/multi/general/execute(аналог execute) – выполнить cmd команду в консоли жертвы;
run post/windows/gather/enum_termserv – получить список серверов к которым коннектилась жертва;
run post/windows/gather/enum_tokens – перечислить токено — залогиненных пользователей в системе;
run post/windows/gather/enum_trusted_locations – получить интересные пути к файлам;
run post/multi/manage/play_youtube – запустить видео в ютуб;
run post/multi/manage/record_mic – запись звука с микрофона. Параметр задает время записи;
run post/multi/manage/set_wallpaper – установить СВОИ обои;
run post/windows/gather/forensics/duqu_check – проверить на уязвимость в Word при замене параметра Trueype;
run post/multi/recon/local_exploit_suggester – прочекать систему на некоторые сплоиты;
run post/windows/gather/forensics/enum_drives — перечисление драйверов работает криво;
run post/windows/capture/keylog_recorder – классный кейлоггер;
run post/windows/capture/lockout_keylogger ещё кейлоггер по мощнее;
run post/windows/escalate/droplnk — создает вредный ярлычок, который если жертва запустит получим админа работает до win7;
run post/windows/gather/hashdump – получить хэши паролей;
run post/windows/escalate/getsystem – стандартная повышалка привелегий, работает очень редко;
run post/windows/escalate/golden_ticket — отличный способ эскалации в доменах;
run post/windows/escalate/ms10_073_kbdlayout – ещё один способ эскалации эксплоит до win7;
run post/windows/escalate/screen_unlock — залочить текущий момнитор;
run post/windows/gather/memory_grep – поиск утечет памяти в процессе;
run post/windows/gather/ad_to_sqlite – Вся информация об Active directory в базу;
run post/windows/gather/bitcoin_jacker – очень повезёт если схватите тачку на которой майнят биткоины;
run post/windows/gather/phish_windows_credentials – фишинговая форма входа на powershell после ввода пасса отдаёт обратно хакеру;
run post/windows/gather/checkvm — проверить не на виртуалке ли мы;
run post/windows/gather/screen_spy – типа скриншотера, делает 1 скрин в секунду и создается иллюзия наблюдения за столом;
run post/windows/gather/smart_hashdump если не работает хэшдамп можно попробовать;
run post/windows/gather/credentials/bulletproof_ftp – парольчики с этого клиента;
run post/windows/gather/tcpnetstat – получаем аналог команды netstat;
run post/windows/gather/usb_history – Информация о флешках побывавших в компьютере и устройствах;
run post/windows/gather/win_privs – Права текущего пользователя;
run post/windows/gather/credentials/domain_hashdump — получить хэшик группы в адешке;
run post/windows/gather/credentials/enum_cred_store – пытаемся брутфорснуть креды пользователей;
run post/windows/gather/credentials/enum_cred_store – пытаемся брутфорснуть креды пользователей;
run post/windows/manage/add_user_domain –Добавляем пользователя в домен;
run post/windows/manage/autoroute – хотим начать хекать хосты на нашей атакованной машине, так проложить маршруты надо сначала;
run post/windows/gather/credentials/enum_picasa_pwds воруем пароли от пикасы, надо мигрировать в explorer;
run post/windows/gather/credentials/filezilla_server – чекаем на наличие файлзиллы;
run post/windows/manage/delete_user – удалить пользователя;
run post/windows/manage/download_exec – скачать и запустить;
run post/windows/manage/enable_rdp включаем РДП;
run post/windows/gather/credentials/gpp — получаем групповые политики в домене;
run post/windows/manage/enable_support_account – открыть саппорт аккаунт;
run post/windows/gather/credentials/heidisql – получить паролики от Heidi;
run post/windows/manage/exec_powershell моя любимая фитчка, выполнить ps команду;
run post/windows/manage/forward_pageant – пропускаем ssh через себя;
run post/windows/manage/inject_ca – очень классная фитча позволяет внедрить свой са сертификат и имея у себя приватный и публичный ключ расшифровывать SSL трафик;
run post/windows/manage/inject_host — внедрить host в файл hosts;
run post/windows/manage/killav попытка задушить популярные процессы;
run post/windows/manage/migrate – мигрировать в процесс, скрывает процесс шелкода, а так же позволяет повысить привилегии и закрепиться. Многие фитчи не работают из другого процесса;
run post/windows/manage/multi_meterpreter_inject – очень полезная фитча, когда нужно внедрить другой payload например выше разрядностью;
run post/windows/gather/credentials/outlook – получить список конфигов в outlook;
run post/windows/manage/payload_inject — аналогично multi_meterpreter_inject но как видно из названий ОС зависимый;
run post/windows/gather/credentials/skype — украсть пароли в скайп;
run post/windows/manage/powershell/build_net_code – Скомпилировать .Net файл с помощью компилятора powershell, очень удобно чтобы пробросить свой код на C#;
run post/windows/manage/powershell/exec_powershell – хотим выполнить ps команду не проблема. По умолчанию валит ошибку но команду все равно выполняет;
run post/windows/manage/priv_migrate – ЭСКАЛАЦИЯ пытается мигрировать в привилегированный процесс, что после миграции дает права пользователя с бОльшими
привилегиями;
run post/windows/gather/credentials/steam – ВОРУЕЕЕМ ПАРОЛИИ СТИИИИМММ;
run post/windows/gather/credentials/tortoisesvn – пытаемся вытянуть конфиги к репам из известного клиента SVN Turtoise;
run post/windows/manage/reflective_dll_inject – DLL Инъекция в процесс;
run post/windows/manage/remove_ca – удалить са поможет для того чтобы сломать ssl и выпустить новый;
run post/windows/gather/credentials/vnc – получить креды от vnc;
run post/windows/manage/rpcapd_start — пишем траффик с удаленной тачки;
run post/windows/gather/credentials/windows_autologin – получить креды автологина очень часто используется;
run post/windows/manage/sticky_keys – ОТЛИЧНЫЙ ПЕРСИСТЕНС срабатывает когда нажат SHIFT 5 раз или горячие клавиши с WINDOWS;
run post/windows/manage/wdigest_caching – фитча, с помощью которой, мы можем получить пароли пользователя плейнтекстом с помощью mimikatz;
run post/windows/manage/webcam Сфоткаемся? ;) > webcam_snap -i 1 -v false ;
run post/windows/gather/enum_applications – получить список установленных тулз;
run post/windows/gather/enum_av_excluded – получения программы в исключениях антивируса удобно для миграции и ав бйпасса;
run post/windows/gather/enum_chrome — работа с хром;
run post/windows/gather/enum_db – Установленные базы данных;
````
<h1 align="center"> MSF Exploit Dev Cheatsheet </h1> <br>
<p align="center">
  <a>
    <a href="https://github.com/Ondrik8/metasploit/blob/master/msf_dev.docx">
    <img src="https://github.com/redcode-labs/msf_dev_cheatsheet/raw/master/img.png" width="500" height="600">
  </a>
</p>



<p>
  This document is a reference that congregates various functions, variables, code snippets and tips that are useful when writing exploits using Metasploit Framework. It isn't completed yet (or even half-way done) so each and every pull request is welcome.
</p>
