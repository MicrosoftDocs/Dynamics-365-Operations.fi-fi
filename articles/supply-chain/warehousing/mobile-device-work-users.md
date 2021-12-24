---
title: Mobiililaitteen käyttäjätilit
description: Tässä aiheessa kuvataan, miten määritetään ja hallitaan käyttäjätilejä, joiden avulla käyttäjät voivat kirjautua ja käyttää varastosovellusta.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f3a930814a1fb98e3b1611adf309c10e66b49b9d
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902094"
---
# <a name="mobile-device-user-accounts"></a>Mobiililaitteen käyttäjätilit

[!include [banner](../includes/banner.md)]

Aina, kun työntekijä alkaa käyttää varastosovellusta, hänen on kirjauduttava sisään käyttäen käyttäjänimeä ja salasanaa. Kullekin järjestelmän työntekijälle voi määrittää minkä tahansa määrän varastosovelluksen käyttäjiä, ja kullekin näistä varastosovelluksen käyttäjälle määritetään yleensä varastoja. Jokaiselle työntekijälle määritetään myös erilaisia asetuksia, joilla luodaan oletusasetukset, sekä muita asetuksia, jotka liittyvät varastosovelluksen käyttöön.

## <a name="set-up-the-required-worker-and-employee-records"></a>Tarvittavien työntekijätietueiden määrittäminen

Ennen kuin voit määrittää varastosovelluksen käyttäjiä, kunkin työntekijän on oltava olemassa Supply Chain Management työntekijänä **Henkilöstöhallinto**-moduulissa.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Mobiililaitteen käyttäjätilien määrittäminen

Kun tarvittavat työntekijät on määritetty henkilöstöhallinnassa, voit määrittää kullekin työntekijälle varastosovelluksen käyttäjiä ja määrittää muita asetuksia, jotka vaikuttavat sovelluksen käyttöön.

1. Valitse **Varastonhallinta \> Asetukset \> Työntekijä**.
1. Jos haluat muokata aiemmin luotua työntekijää, valitse hänet luetteloruudusta. Voit lisätä uuden tietueen valitsemalla toimintoruudusta **Uusi**.
1. Jos määrität uuden työntekijän, noudata seuraavia ohjeita:

    1. Valitse **Työntekijä**-kentässä kohdekäyttäjä työntekijäluettelossa.
    1. Valitse **Valitse**.
    1. Valitse toimintoruudussa **Tallenna**.

1. Oletusprofiilin avulla varastotyöntekijää voidaan ohjata pakkausasemalla siellä vaadittavan prosessin läpi. Vaihtoehtoisesti oletusprofiilin avulla voidaan tallentaa työntekijän ensisijaiset profiiliasetukset. Valitse **Profiili**-pikavälilehdellä seuraavat lisäkentät:

    - **Kontin pakkauskäytäntö** – Valitse kontin pakkauskäytäntö, jolla määritellään, miten kontit käsitellään pakkausasemalla. Tässä valittu kontin pakkauskäytäntö valitaan työntekijälle ennalta, kun hän avaa pakkausaseman. Lisätietoja on seuraavassa blogikirjoituksessa: [Parannettu pakkaustoiminto](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611),
    - **Pakkausprofiilin tunnus** – Valitse pakkausprofiilin tunnus, jolla määritetään pakkauskäytäntö ja käytettävät konttiasetukset. Jos valittu pakkausprofiilin tunnus on liitetty kontin pakkauskäytäntöön, et voi muuttaa **Kontin pakkauskäytäntö** -asetusta tällä sivulla.

1. Määritä **Oletuspakkausasema**-pikavälilehdessä seuraavat kentät määrittääksesi oletuspakkausasema, jota käytetään, kun työntekijä kirjautuu sisään. Työntekijä voi kuitenkin valita tarpeen mukaan toisen pakkausaseman.

    - **Toimipaikka** – Valitse toimipaikka, jossa oletuspakkausasema sijaitsee.
    - **Varasto** – Valitse varasto, jossa oletuspakkausasema sijaitsee.
    - **Sijainti** – Valitse oletuspakkausaseman sijainti.

1. **Käyttäjät**-pikavälilehdessä voit luoda minkä tahansa määrän varastosovelluksen käyttäjätilejä valitulle työntekijälle. Kukin tili on yhdistetty tiettyyn varastoon tai tiettyihin varastoihin. Työkalupalkin avulla voit lisätä tai poistaa käyttäjätilejä, nollata valitun tilin salasanan tai määrittää varastoja valitulle tilille. Määritä kullekin käyttäjätileille seuraavat kentät:

    - **Käyttäjätunnus** – Anna yksilöivä tunnus.
    - **Käyttäjänimi** – Anna tunnukselle nimi.
    - **Oletusvarasto** – Määritä oletusvarasto, jossa työntekijä yleensä työskentelee. Työkalupalkin avulla voit määrittää lisää varastoja, ja työntekijä voi vaihtaa varastojen välillä käyttämällä mobiililaitteen valikkokohteen epäsuoraa **Vaihda varastoa** -toimintoa.
    - **Valikon nimi** – Valitse päävalikko, jota käytetään työntekijän aloitussivuna. Mahdollisuus määrittää päävalikko kullekin työntekijälle on hyödyllinen, koska sillä voidaan hallita kunkin työntekijän käytössä olevaa valikkorakennetta. Esimerkiksi vain lähtevien alueella toimivien työntekijöiden valikkoa voi mukauttaa sellaisia tehtäviä varten, jotka liittyvät kyseisen alueen lähtevien toimintoihin.
    - **Ei käytössä** – Valittu valintaruutu ilmaisee, että käyttäjätili ei ole käytössä. Käyttäjätili poistetaan automaattisesti käytöstä, jos työntekijä kirjoittaa varastosovelluksen riville väärän salasanan viisi kertaa. Tämän valintaruudun voi kuitenkin valita myös manuaalisesti. Poista valintaruudun valinta, jos haluat ottaa käyttäjän jälleen käyttöön.

1. Määritä **Työ**-pikavälilehdessä seuraavat kentät:

    - **Salli keräilysijainnin ohitus** – Määritä tämän asetuksen arvoksi *Kyllä*, jotta työntekijä voi ohittaa keräilyvaiheiden sijainnin. Tämä ominaisuus voi olla hyödyllinen, jos fyysinen varasto ei vastaa järjestelmän ehdottamaa sijaintia.
    - **Salli hyllytyssijainnin ohitus** – Määritä tämän asetuksen arvoksi *Kyllä*, jotta työntekijä voi ohittaa hyllytysvaiheiden sijainnin. Tämä ominaisuus voi olla hyödyllinen, jos ehdotettu hyllytyssijainti ei ole käytettävissä tai jos valmistelusijainnit ovat muuttuneet.
    - **Salli myynnin ylikeräily** – Määritä tämän asetuksen arvoksi *Kyllä*, jotta työntekijä voi ylikeräillä myyntitilausten yhteydessä. Lisätietoja: [Myyntitilausten ja siirtotilausten ylikeräily](over-picking-for-sales-and-transfer-orders.md).
    - **Salli siirtotilauksen ylikeräily** – Määritä tämän asetuksen arvoksi *Kyllä*, jotta työntekijä voi ylikeräillä siirtotilausten yhteydessä. Lisätietoja: [Myyntitilausten ja siirtotilausten ylikeräily](over-picking-for-sales-and-transfer-orders.md).
    - **Salli työhön liitetyn varaston siirto** – Määritä tämän asetuksen arvoksi *Kyllä*, jotta työntekijä voi siirtää varastoa, joka on jo varattu tai liitetty muuhun työhön. Lisätietoja: [Työhön liitetyn varaston siirtäminen varastonhallinnassa](move-inventory-associated-work.md).
    - **Salli manuaalinen nimikkeen uudelleenkohdistus** – Määritä tämän asetuksen arvoksi *Kyllä*, jotta työntekijä voi suorittaa manuaalisen uudelleenkohdistuksen lyhyen keräilyn yhteydessä. Nimikkeen uudelleenkohdistus opastaa työntekijät keräilemään varastoa toisesta sijainnista. Vaikka automaattinen uudelleenkohdistus on kaikkien työntekijöiden käytettävissä, manuaalinen uudelleenkohdistus vaatii työntekijälle nimenomaista määritystä. Kunkin työntekijän manuaalisen uudelleenkohdistuksen hallinta voi olla hyödyllistä, koska sen avulla voit hallita näkyvyyttä kunkin työntekijän osalta esimerkiksi silloin, kun nimikkeiden keräily karanteeni- tai irtotavara-alueelta on rajoitettu luotettaviin työntekijöihin. Lisätietoja esitetään seuraavassa blogikirjoituksessa: [Automaattinen ja manuaalinen nimikkeiden uudelleenkohdistus lyhyen keräilyn yhteydessä](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **On inventoinnin valvoja** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat tehdä työntekijästä inventoinnin valvojan. Tällöin kaikki inventoinnit, jotka työntekijä suorittaa varastosovelluksessa, hyväksytään heti. Kenttiä **Enimmäisprosenttiraja**, **Enimmäismääräraja** ja **Enimmäisarvoraja** ei oteta huomioon sellaisten työntekijöiden osalta, joille tämän asetuksen arvoksi on määritetty *Kyllä*.
    - **Enimmäisprosenttiraja** – Kirjoita suurin prosenttimäärä, jonka inventointi voi poiketa oletetusta määrästä ilman, että vaaditaan hyväksyntä inventoinnin esimieheltä.
    - **Enimmäismääräraja** – Syötä kokonaismäärä, jonka syötetty määrä voi poiketa odotetusta määrästä (yksikköinä) ilman, että vaaditaan hyväksyntä inventoinnin esimieheltä.
    - **Enimmäisarvoraja** – Kirjoita enimmäismäärä, jonka varastokustannus voi poiketa oletetusta kustannuksesta ilman, että vaaditaan hyväksyntä inventoinnin esimieheltä.

1. Valitse toimintoruudussa **Tallenna**.
1. Jos olet lisännyt uuden käyttäjätilin, voit luoda avautuvassa **Määritä salasana** -valintaikkunassa yksinkertaisen salasanan, jolla käyttäjä voi kirjautua mobiilisovellukseen. Kirjoita yksinkertainen salasana kaksi kertaa ja jatka valitsemalla **Tallenna salasana**.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Kunkin varastosovelluksen käyttäjän kielen, numeromuotojen ja aikavyöhykkeen määrittäminen

Kun työntekijä kirjautuu Warehouse Management -mobiilisovellukseen, kieli, numeromuodot ja aikavyöhyke muuttuvat vastaamaan työntekijän asetuksia. Vaiheen 3 osassa [Mobiililaitteiden käyttäjätilien määrittäminen](#set-wma-users) valitut työntekijän tiliasetukset määrittävät käytettävät asetukset. Jos tarvitset kullein käyttäjälle erilliset asetukset, käytä eri työntekijätilejä. Seuraavassa esitetään, miten kunkin varastosovelluksen käyttäjän kieli, numeromuodot ja aikavyöhyke voidaan vaihtaa.

1. Valitse **Varastonhallinta \> Asetukset \> Työntekijä**.
1. Etsi sen työntekijän nimi, jonka haluat määrittää. Varmista, että työntekijällä on kaikki pakolliset **Käyttäjät**-pikavälilehdessä luetellut varastosovelluksen käyttäjätilit. Luo uusi työntekijä ja/tai lisää varastosovelluksen käyttäjätilejä tarpeen mukaan noudattamalla osan [Mobiililaitteiden käyttäjätilien määrittäminen](#set-wma-users) vaiheita.
1. Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.
1. Valitse käyttäjätili, jossa **Henkilö**-sarakkeessa näkyy vaiheessa 2 etsimäsi työntekijän nimi.

    > [!IMPORTANT]
    > **Käyttäjät**-sivulla näkyvät **Käyttäjätunnus**-arvot *eivät* liity arvoon, joka näkyy vaiheessa 1 avatun **Työntekijä**-sivun **Käyttäjät**-pikavälilehdissä.

1. Valitse toimintoruudussa **Käyttäjän asetukset**.
1. Määritä **Astukset**-välilehdessä seuraavat kentät:

    - **Kieli** – Valitse käyttäjän ensisijainen kieli. Tällä kentällä hallitaan myös varastosovelluksessa näkyvää päivämäärän muotoa.
    - **Päivämäärä-, aika- ja numeromuoto** – Valitse kieli, joka määrittää varastosovelluksessa näkyvät numeromuodot. Huomaa, että varastosovelluksessa näkyvät päivämäärä- ja aikamuodot määräytyvät itse asiassa **Kieli**-kentän eivätkä tämän kentän mukaan.
    - **Aikavyöhyke** – Valitse aikavyöhyke, jolla työntekijä työskentelee. Tämä kenttä vaikuttaa kaikkien niiden rekisteröintien aikaleimoihin, jotka työntekijä tekee sovelluksella.

> [!NOTE]
> Joissakin tapauksissa varastosovellus ei voi etsiä tiettyjä työntekijöiden asetuksia, jotka määrittävät kielen, numeromuodot ja aikavyöhykkeen. Seuraavat säännöt pätevät:
>
> - Jos sovellusta ei ole liitetty Supply Chain Management -ympäristöön (esimerkiksi kun sovellus käynnistetään ensimmäisen kerran sen asennuksen jälkeen), käytetään paikallisen laitteen kieltä. Kun laitteen kieli muuttuu, myös sovelluksen kieli muuttuu. Lisätietoja paikallisen laitteen kielen määrittämisestä on laitteen ja/tai käyttöjärjestelmän ohjeissa.
> - Jos sovellus on liitetty Supply Chain Management -ympäristöön mutta kirjautuneelle työntekijälle ei ole määritetty asetuksia, kieli, numeromuodot ja aikavyöhyke valitaan sen tilin mukaan, joka on yhdistetty siihen asiakastunnukseen, jota kyseinen laite käyttää Supply Chain Management -yhteyden luomiseen. Lisätietoja: [Supply Chain Managementin käyttäjätilin luominen ja määrittäminen](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Jos huomaat, että varastosovelluksella tehdyissä rekisteröinneissä näkyy virheellisiä aikaleimoja, sinun voi olla tarpeen muuttaa sille käyttäjätilille määritettyä aikavyöhykettä, jota työntekijät käyttävät Supply Chain Managementiin kirjautumiseen ja/tai siihen liittyvään todennukseen. Kuten edellä mainittiin, aikavyöhykeasetus voi perustua käyttäjätiliin, jota käytetään **Työntekijä**-sivun mukaisesti varastosovellukseen kirjautumiseen. Vaihtoehtoisesti, jos käyttäjätiliä ei ole määritetty **Työntekijä**-sivulla, aikavyöhyke perustuu käyttäjätiliin, joka on yhdistetty asiakastunnukseen, jota käytetään todennukseen, kuten **[Azure Active Directory -sovellukset](install-configure-warehouse-management-app.md)** -sivulla on määritetty.
