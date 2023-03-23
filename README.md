# Onlinebutik API

<b>Syfte</b>: Skapa ett enkelt onlinebutik-API med C# och .NET som låter användare hantera produkter och beställningar.

<b>Varaktighet</b>: 4 timmar

<b>Verktyg/Tekniker</b>: C#, .NET, ASP.NET Core, Entity Framework Core, MS SQL Server (eller annan föredragen databas)

## Instruktioner:

1. Skapa ett nytt ASP.NET Core Web API-projekt.
2. Konfigurera en ny databas med Entity Framework Core.
3. Utforma och implementera följande databasmodeller:
- Product
    - Id (int, primärnyckel)
    - Name (sträng, obligatorisk)
    - Description (sträng)
    - Price (decimal, obligatorisk)
    - Stock (int, obligatorisk)
    - ImageUrl (sträng)
- Order
    - Id (int, primärnyckel)
    - CustomerName (sträng, obligatorisk)
    - CustomerEmail (sträng, obligatorisk)
    - TotalAmount (decimal, obligatorisk)
    - CreatedAt (DateTime, obligatorisk)
    - OrderItems (List\<OrderItem\>, obligatorisk)
- OrderItem
    - Id (int, primärnyckel)
    - OrderId (int, främmande nyckel till Order)
    - ProductId (int, främmande nyckel till Product)
    - Quantity (int, obligatorisk)
    - Price (decimal, obligatorisk)
4. Implementera följande API-slutpunkter:
- Products
    - GET /api/products: Hämta en lista över alla produkter
    - GET /api/products/{id}: Hämta en enskild produkt med dess ID
    - POST /api/products: Lägg till en ny produkt
    - PUT /api/products/{id}: Uppdatera en befintlig produkt
    - DELETE /api/products/{id}: Ta bort en produkt
- Orders
    - GET /api/orders: Hämta en lista över alla beställningar
    - GET /api/orders/{id}: Hämta en enskild beställning med dess ID
    - POST /api/orders: Lägg till en ny beställning (se till att lager uppdateras)
    - DELETE /api/orders/{id}: Ta bort en beställning (se till att lager uppdateras)        
5. Implementera nödvändiga valideringskontroller och felhantering för API-slutpunkterna.
6. Skriv enhetstester för att täcka huvudfunktionaliteten i API:et.
7. Dokumentera dina API-slutpunkter med Swagger eller liknande verktyg.

## Leveranser:

1. Den kompletta källkoden för den implementerade lösningen.
2. En README-fil med instruktioner om hur man konfigurerar och kör projektet, inklusive eventuell databasinställning.

## Utvärderingskriterier:

1. Kvalitet och organisering av koden
2. Korrekt implementering av de angivna databasmodellerna och API-slutpunkterna
3. Valideringskontroller och felhantering
4. Enhetstesttäckning
5. API-dokumentation
