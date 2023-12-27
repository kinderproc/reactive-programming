It's a project that implements task from Iton company interview.
Contacts: HR Элла +7 922 886 6096

Task:
Дано:
- метод Flux<StockPrice> getActiveStockPrices() - возвращает каждые 100 мс акцию с ценой в долларах, { name: VTB, price: 23 },  { name: LUKOIL, price: 100 }...
- метод Flux<ExchangeRate> getExchangeRate() - возвращает каждые 200 мс обновленный курс одной из валюты { name: RUB, rate: 89 }, { name: USD, rate: 1 }, { name: EUR, rate: 104}...
- метод Flux<StockPriceRub> getActualStockPrices() {}

@Data
class StockPrice {
private String name;
private Long price;
}

@Data
class ExchangeRate {
private String name;
private Long rate;
}

@Data
class StockPriceRub {
private String name;
private Long priceRub;
private String op;
}

Задача

реализовать метод getActualStockPrices
цену каждой акции привести к рублю, если текущая цена акции выше предыдущей, в StockPriceRub.op записать +, если меньше -, если равна ""

