


1. Получи список доступных дисков:

```bash
diskutil list
```

2. Зашифруй диск:

```bash
diskutil apfs encryptVolume diskXsY -userDiskPassword
```

   - Замените `diskXsY` на идентификатор вашего диска.

3. Проверь статус шифрования:

```bash
diskutil apfs list
```


**Настройка удаления данных после 5 попыток (с помощью MDM или команд)**

Для более точной настройки (например, удаление данных после 5 попыток), потребуется использование **командной строки** или **Mobile Device Management (MDM)**.

Настройка через `sysadminctl`:

1. Открой Terminal.
    
2. Установи ограничение для числа попыток входа:

```bash
sudo sysadminctl -adminUser <admin_username> -adminPassword <admin_password> -setMaxFailedLogins 5
```

После 5 неудачных попыток macOS автоматически заблокирует учетную запись или начнет выполнение настроенных действий.