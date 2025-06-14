# **Biblioteka SLU: API**

Moduł API zapewnia konkretne implementacje i klasy pomocnicze, które upraszczają dostęp do surowego API, służąc jako wygodna alternatywa dla
twórców widżetów.

## **Przeznaczenie**

- Wdraża interfejsy z `/types` z klasami gotowymi do użycia
- Ukrywa złożone API niskiego poziomu
- Zapewnia metody dla często wykonywanych operacji
- Służy jako podstawowa warstwa interakcji między widżetami i aplikacją SLU

## **Zastosowanie**

W razie potrzeby możesz użyć biblioteki. Oto podstawowy przykład:

```ts
import { StructClass } from "@seelen-ui/lib/api";

const widgetApi: StructClass = await StructClass.geAsync();
const something = widgetApi.getSomething();
const somethingAsync = await widgetApi.getSomethingAsync();

await widgetApi.doSomething();
```

## **Ważne notatki:**

1. Ta biblioteka API działa tylko w środowisku wykonawczym widżetów Seelen UI
2. Przy próbie użycia go w Node.js lub w przeglądarce wystąpią błędy
3. Widżety korzystające z tego API muszą być zaktualizowane, aby działały poprawnie z
   najnowszą wersją Seelen UI