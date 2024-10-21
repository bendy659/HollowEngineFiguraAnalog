# Отдельная директория под аватары

---

## Инициализатор аватара

> Для того чтобы аватар был доступен был в списке, нужно чтобы в спец. директории в
отдельной папке для каждого аватара (пример: `he_avatars/my_avatar`) был файл к примеру:
`avatar.json` или можно тоже сделать как скрипт `avatar.kts`.

> Если же систему будет работать на скриптах, то можно реализовать типо такого метода:
> ```kts
> val avatar by HEAvatarHelper(id: Int/String)
> ```

---

## Данные аватара

> - Обычная информация:
>   - Имя аватара, `name: String` | `"name": "MyAvatar"` / `avatar.name("MyAvatar")`.
>   - Описание аватара, `desc: String` | `"desc": "AvatarDesc"` / `avatar.desc("AvatarDesc")`.
>   - Автор, `author: String` | `"author": "Me"` / `avatar.author("Me")`.
> 
> - Расширенная информация:
>   - Стандартная модель аватара: `model: Path` | `"default_model":"./avatar_model.gltf"` /
`avatar.defaulModel("./avater_model.gltf")`.
>   - Регистрация кейбиндов: `newKeybind: Keybind` |
> ```json
> "keybinds": [
>   { "key": "GLWF_KEY_F12", "id": "my-keybind-f12" }
> ]
> ```
> ```kts
> val exampleKeybind = HEAvaterHelper.Keybind(key: GLWF)
> 
> val myKeybindF12 = HEAvaterHelper.Keybind(GLWF.GLWF_KEY_F12)
> ```