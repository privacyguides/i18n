---
title: "Miért fontos az adatvédelem"
icon: 'material/shield-account'
---

A digitális adatokkal való visszaélések modern korában az adatvédelmed még soha nem volt ennyire kritikus, mégis sokan úgy gondolják, hogy ez már egy veszett ügy. Nem az. ==A magánéleted veszélyben van==, és törődnöd kell vele. A adatvédelem a hatalomról szól, és nagyon fontos, hogy ez a hatalom a megfelelő kezekbe kerüljön.

A magánélet végső soron az emberi információkról szól, és ez azért fontos, mert tudjuk, hogy az emberi információk hatalmat biztosítanak emberi lények felett. Ha fontos számunkra, hogy képesek legyünk hiteles, kiteljesedett és szabad emberek lenni, akkor törődnünk kell a rólunk szóló információkra vonatkozó szabályokkal. Modern társadalmunk nagy része **információ** köré épül. Amikor vásárolsz online, híreket olvasol, utánanézel valaminek, szavazol, útbaigazítást kérsz, vagy bármi mást csinálsz, akkor információra támaszkodsz. Ha egy információs társadalomban élünk, akkor az információink számít, és ebből kifolyólag az adatvédelem is számít.

## Mi az adatvédelem?

Sokan összekeverik az **adatvédelem**, az **adatbiztonság** és az **anonimitás** fogalmát. Láthatod, hogy emberek kritizálnak különböző termékeket, mint "nem privát", amikor valójában úgy értik, hogy nem biztosít anonimitást például. Ezen a weboldalon mindhárom témakörrel foglalkozunk, de fontos, hogy megértsd a köztük lévő különbséget, és hogy mikor melyik kerül a képbe.

**Adatvédelem**
:

==Az adatvédelem az a biztosíték, hogy az adataidat csak azok a felek láthatják, akiknek látni szándékozod azokat.== Az azonnali üzenetküldő szolgáltatások esetében például az end-to-end titkosítás biztosítja az adatvédelmet, mivel az üzenetet csak te és a címzett láthatja.

**Adatbiztonság**
:

A biztonság az a képesség, hogy megbízhatsz az általad használt alkalmazásokban - hogy az érintett felek azok, akiknek mondják magukat -, és hogy ezeket az alkalmazásokat biztonságosként tudod tartani. A webes böngészés konteksztusában például a biztonságot a HTTPS tanúsítványok nyújthatják.
:

A tanúsítványok bizonyítják, hogy közvetlenül a meglátogatott webhelyhez beszélsz, és megakadályozzák, hogy a hálózaton lévő támadók elolvassák vagy módosítsák a webhelyre küldött vagy onnan származó adatokat.

**Anonimitás**
:

Az anonimitás az a képesség, hogy állandó azonosító nélkül tevékenykedjünk. Ezt online a [Tor](../tor.md) segítségével érheted el, amely lehetővé teszi, hogy egy saját IP-cím és hálózati kapcsolat helyett egy véletlenszerű IP-címmel és hálózati kapcsolattal böngészhesd az internetet.
:

A **Pszeudonimitás** hasonló elképzelés, de lehetővé teszi, hogy állandó azonosítóval rendelkezz anélkül, hogy az a valódi személyazonosságodhoz kötődne. Ha mindenki `@GamerGuy12` néven ismer téged online, de senki sem tudja az igazi nevedet, akkor ez az álneved.

Mindezek a fogalmak átfedik egymást, de ezek bármilyen kombinációja lehetséges. A legtöbb ember számára az a legtökéletesebb, amikor mindhárom fogalom átfedésben van. Ezt azonban nehezebb elérni, mint azt sokan kezdetben gondolnák. Néha áldozatot kell hoznod ezek közül néhányon, és teljesen rendben van. This is where **threat modeling** comes into play, allowing you to make informed decisions about the [software and services](../tools.md) you use.

[:material-book-outline: Learn More About Threat Modeling](threat-modeling.md ""){.md-button}

## Privacy vs. Secrecy

A common counter-argument to pro-privacy movements is the notion that one doesn't need privacy if they have **"nothing to hide."** This is a dangerous misconception, because it creates a sense that people who demand privacy must be deviant, criminal, or wrong.

==You shouldn't confuse privacy with secrecy.== We know what happens in the bathroom, but you still close the door. Ez azért van, mert magánéletet akarsz, nem titoktartást. There are always certain facts about us—say, personal health information, or sexual behavior—that we wouldn't want the whole world to know, and that's okay. The need for privacy is legitimate, and that's what makes us human. Privacy is about empowering your rights over your own information, not about hiding secrets.

## Is Privacy About Control?

A common definition of privacy is that it is the ability to *control* who has access to your data. This is an easy trap to fall into, in fact it is the definition of privacy we operated this website on for a long time. It sounds nice, and it appeals to many people, but in practice it just doesn't work.

Take cookie consent forms, for example. You may encounter these dozens of times per day on the various websites you visit, with a nice array of checkboxes and sliders which allow you to "curate" your preferences to exactly fit your needs. In the end, we just hit the "I Agree" button, because we just want to read the article or make a purchase. Nobody wants to complete a personal privacy audit on every single website they visit. This is an exercise in [choice architecture](https://en.wikipedia.org/wiki/Choice_architecture), designed to make you take the easy route out instead of delving into a maze of configuration options that don't need to exist in the first place.

==Control over your privacy inside most apps is an illusion.== It's a shiny dashboard with all sorts of choices you can make about your data, but rarely the choices you're looking for, like "only use my data to help me." This type of control is meant to make you feel guilty about your choices, that you "had the choice" to make the apps you use more private, and you chose not to.

Privacy is something we need to have baked into the [software and services](../tools.md) we use by default, you can't bend most apps into being private on your own.

## Sources

- [Why Privacy Matters](https://www.amazon.com/Why-Privacy-Matters-Neil-Richards/dp/0190939044) (2021) by Neil Richards
- [The New Oil: Why Privacy & Security Matter](https://thenewoil.org/en/guides/prologue/why/)
- [@Thorin-Oakenpants on GitHub](https://github.com/privacytools/privacytools.io/issues/1760#issuecomment-597497298)
