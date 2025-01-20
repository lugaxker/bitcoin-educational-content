---
term: SHA256

---
Zkratka pro "*Secure Hash Algorithm 256 bits*". Jedná se o kryptografickou hašovací funkci, která vytváří 256bitový digest. Byla navržena *Národní bezpečnostní agenturou* (NSA) na počátku roku 2000 a stala se federálním standardem pro zpracování citlivých dat. V protokolu Bitcoin je funkce `SHA256` všudypřítomná. Používá se k hašování hlaviček bloků jako součást důkazu práce. funkce `SHA256` se používá také při odvozování přijímací adresy z veřejného klíče. Dále se používá pro agregaci transakcí a svědků v rámci Merklových stromů v blocích. `SHA256` se vyskytuje také při výpočtu otisků klíčů, výpočtu některých kontrolních součtů a v mnoha dalších procesech kolem Bitcoinu. Při použití dvakrát po sobě se označuje jako `HASH256`. Tato dvojí aplikace se u Bitcoinu používá převážně. Když se `SHA256` používá ve spojení s funkcí `RIPEMD160`, označuje se jako `HASH160`. Toto dvojité hašování se používá pro otisky klíčů a pro hašování veřejných klíčů. Funkce `SHA256` je součástí rodiny SHA 2.