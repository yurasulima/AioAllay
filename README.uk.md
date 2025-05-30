AioAllay WIP


> 🌐 [English](./README.en.md) | 🇺🇦 [Українська](./README.uk.md)



AioAllay — це асинхронний клієнт для взаємодії з API майнкрафт бедрок сервера [Dangerous](https://mblueberry.fun).

Можливості

    🌀 Асинхронність (на базі aiohttp)

    🛠️ Легка інтеграція в asyncio-застосунки

    📦 Взіємодія з профілями користувачів, замовленнями, логами, тощо 

Встановлення

pip install aioallay

Або зі сховища:

git clone https://github.com/yurasulima/AioAllay.git
cd AioAllay
pip install .

Приклад використання

    import asyncio
    from typing import List
    from aioallay.types import User
    from aioallay import Client
    
    TOKEN = "your-token"
    
    client = Client(token=TOKEN)
    
    async def main() -> None:
        users: List[User] = await client.get_all_user()
        print(users)
    
    if __name__ == "__main__":
        asyncio.run(main())

Вимоги

    Python 3.10 або вище
    pydantic~=2.11.5
    aiohttp~=3.10.11



Ліцензія

MIT © Юрій Сулима