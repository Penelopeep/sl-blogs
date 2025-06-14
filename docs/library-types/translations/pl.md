# **Biblioteka SLU: Typy i interfejsy**

Moduł `types` biblioteki SLU zapewnia kolekcję definicji niezbędnych typów i
interfejsów, które służą jako podstawa do tworzenia widżetów. Ten moduł oferuje:

- Znormalizowane definicje typów używane w ekosystemie Seelen UI
- Zapewnia interfejsy do spójnej implementacji widżetu
- Gwarantuje bezpieczeństwo typów w podczas rozwoju widżetu
- Służy jako wspólna komunikacja między podstawową aplikacją a widżetami

## **Zastosowanie**

```ts
import { StructInterface } from "@seelen-ui/lib/types";

const myObject: StructInterface = { ... }
```

## **Kluczowe funkcje:**

- **Definicje typów podstawowych**: Podstawowe typy używane przez aplikację
  Seelen UI
- **Komunikacja widżetów**: Interfejsy, które widżety muszą zaimplementować, aby
  uzyskać kompatybilność
- **Udostępnione modele**: Wspólne struktury danych używane na platformie
- **Narzędzia typu**: Typy pomocnicze do rozwoju widżetów

Te typy są używane zarówno wewnętrznie przez aplikację, jak i udostępniane
zewnętrznym deweloperom widżetów, aby zapewnić spójność typów w całym ekosystemie.
