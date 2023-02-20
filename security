import random

# функція генерації ідентифікатора гарантії
def generate_garantee_id():
    return random.randint(100000, 999999)

# функція генерації дати
def generate_date():
    return datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")

# функція генерації гарантії
def generate_garantee(goods, amount, commission_rate, currency):
    # генеруємо ідентифікатор гарантії
    garant_id = generate_garantee_id()
    # генеруємо дату створення гарантії
    date_created = generate_date()
    # розраховуємо комісію за гарантію
    commission = calculate_commission(amount, commission_rate, currency)
    # обчислюємо суму, яка буде заблокована на рахунку користувача
    blocked_amount = amount + commission
    # створюємо словник гарантії
    garant = {
        "id": garant_id,
        "goods": goods,
        "amount": amount,
        "commission": commission,
        "blocked_amount": blocked_amount,
        "currency": currency,
        "date_created": date_created
    }
    return garant

# функція розрахунку комісії за гарантію
def calculate_commission(amount, commission_rate, currency):
    # розраховуємо комісію в залежності від суми угоди та валюти
    if currency == "usdt" and amount < 500:
        return 0
    elif currency == "usdt" and 500 <= amount < 1000:
        return 1
    elif currency == "usdt" and 1000 <= amount < 10000:
        return 3
    elif currency == "usdt" and 10000 <= amount < 100000:
        return amount * 0.0005
    elif currency == "usdt" and amount >= 100000:
       
