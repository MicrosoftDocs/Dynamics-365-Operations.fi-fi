---
title: Ostoskorin ja maksusivun yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen ostoskori- ja kassasivun yleiskatsaus.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e450192025b29c655be49050aa3e61fc8acd898
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982965"
---
# <a name="cart-and-checkout-pages-overview"></a>Ostoskorin ja maksusivun yleiskatsaus

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen ostoskori- ja kassasivun yleiskatsaus.

Sähköisen kaupankäynnin sivuston ostoskorisivulla näkyvät kaikki nimikkeet, jotka asiakas on lisännyt koriin. Ostoskorisivu luodaan ostoskorimoduulin avulla. Ostoskorimoduuli on säilö, joka isännöi kaikkia niitä moduuleja, joita tarvitaan näytettäessä ostoskorin nimikkeet. Ostoskorimoduuli voi käyttää myös muita moduuleja tilauksen yhteenvedon ja mahdollisten asiakastilausta koskevien tarjouskoodien näyttämisessä.

Sähköisen kaupankäynnin sivuston kassasivulla on vaiheittainen työnkulku, jota asiakkaat seuraavat syöttäessään tilauksen tekemisessä vaadittavat tiedot. Kassamoduuli voi sisältää moduuleja, jotka käsittelevät toimitusosoitetta, toimitusmenetelmiä, laskutustietoja, tilauksen yhteenvetoa ja muita asiakastilauksiin liittyviä tietoja.

## <a name="cart-page"></a>Ostoskorisivu

Ostoskorisivu toimii ostoskassina. Se sisältää kaikki ostoskoriin lisätyt nimikkeet.

Seuraavassa kuvassa on esimerkki ostoskorisivusta, joka on luotu verkon moduulikirjaston ja Fabrikam-teeman avulla.

![Esimerkki ostoskorisivusta.](./media/cart2.PNG)

Ostoskorisivun päätekstiosassa näkyvät kaikki nimikkeet, jotka asiakas on lisännyt koriin. Kaikki käytettävissä olevat alennukset ovat esillä. Nämä alennukset sisältävät monimutkaisia alennuksia. Esimerkkejä ovat Osta 3 nimikettä ja saat 10 % alennusta tai Osta pullo ja reppu ja saat 10 % alennusta. Tilauksen yhteenvedon moduulissa on esimerkiksi alennusten, toimituksen ja verojen jälkeen maksettavaksi jäävä summa. Tarjouskoodimoduulin avulla asiakas voi käyttää tarjouskoodeja tai poistaa niitä.

Asiakas voi tehdä ostoksia anonyymisti tai kirjautuneena käyttäjänä. Jos asiakas on kirjautunut sisään, ostoskorin nimikkeet säilytetään istuntojen välillä. Näin asiakas voi jatkaa ostonsa tekemistä useista laitteista.

Ostoskorista asiakas voi jatkaa kassalle. Asiakas voi aloittaa kassalle siirtymisen vieraana tai kirjautuneena käyttäjänä.

Lisätietoja ostoskorisivun muokkaamisesta on kohdassa [Ostoskorimoduulin lisääminen sivulle](add-cart-module.md).

## <a name="checkout-page"></a>Kassasivu

Kassasivulla asiakkaat syöttävät tilauksen tekemisessä vaadittavat tiedot.

Seuraavassa kuvassa on esimerkki kassasivusta, joka on luotu moduulikirjaston avulla.

![Esimerkki kassasivusta.](./media/Checkout.PNG)

Kassasivun päätekstiosa kerää tilauksen tiedot. Näitä tietoja ovat toimitusosoite, toimitusvaihtoehdot ja maksutiedot. Kassalle siirtyminen on vaiheittainen työnkulku, koska tiedot on syötettävä tietyssä järjestyksessä. Esimerkiksi toimitusosoite on syötettävä ennen toimituskustannusten laskemista ja maksun hyväksymistä.

### <a name="shipping-address"></a>Toimitusosoite

Toimitusosoite on pakollinen, jos nimikkeet on toimitettava. Kunkin alueen toimitusosoitteiden muoto voidaan määrittää Dynamics 365 Commerce -sovelluksessa. Jos nimikkeet toimitetaan esimerkiksi Yhdysvaltoihin, toimitusosoitteessa on oltava katuosoite, osavaltio ja postinumero. Toimitusosoitekentille tehdään joitakin perussyötteiden tarkistuksia, kuten aakkosnumeeristen merkkien, enimmäispituuden ja numeroiden tarkistus. Vaikka osoitteen oikeellisuutta ei sinänsä tarkisteta, tämä tarkistus voidaan tehdä käyttämällä mukautettuja kolmannen osapuolen palveluita.

Toimitusosoitetta käytetään kaikissa ostoskorin nimikkeissä, joille on valittu toimitusvaihtoehto. Jos käytössä on kassatyönkulku, joka sisältyy moduulikirjastoon, yksittäisiä ostoskorin nimikkeitä ei voi toimittaa eri osoitteisiin. Jos tarvitset tätä ominaisuutta, se voidaan ottaa käyttöön kassamoduulien mukauttamisen avulla.

Kun toimitusosoite on annettu, Dynamics 365 Commerce -verkkokaupassa käytettävissä olevat toimitustavat ovat näkyvissä. Toimitustavat ja niitä tukevat osoitteet voidaan määrittää Commerce-sovelluksessa.

### <a name="payment"></a>Maksu

Kassatyönkulun seuraava vaihe on maksu. Sähköisessä kaupankäynnissä voidaan käyttää useita maksutapoja, kuten luottokortteja, lahjakortteja ja kanta-asiakkuuspisteitä. Myös näiden toimitustapojen yhdistelmää voidaan käyttää. Käytettävissä olevien toimitustapojen mukaan voidaan tarvita lisätietoja. Esimerkiksi luottokorttimaksu edellyttää laskutusosoitetta. Luottokorttimaksut käsitellään Adyen-maksuyhdistimen avulla.

#### <a name="loyalty-points"></a>Kanta-asiakkuuspisteet

Kassatyönkulun aikana asiakas, joka on kanta-asiakkuusohjelman jäsen ja joka on kerännyt kanta-asiakkuuspisteitä, voi lunastaa pisteet tilausta varten. Kanta-asiakkuuspisteiden moduuli näkyy vain, jos asiakas on kanta-asiakasohjelman jäsen. Tämä moduuli ei näy käyttäjille, jotka eivät ole jäseniä, eikä vierailijoille.

#### <a name="gift-cards"></a>Lahjakortit

Moduulikirjaston avulla voi lunastaa sisäiset lahjakortit tilausta varten. Asiakkaan on kirjauduttava sisään, jotta hän voi käyttää sisäistä lahjakorttia. Lisäsuojausta varten on suositeltavaa mukauttaa työnkulku käyttämällä sisäisissä lahjakorteissa henkilökohtaista tunnuslukua (PIN).

### <a name="signed-in-and-guest-users"></a>Kirjautuneet käyttäjät ja vierailijat

Asiakas voi suorittaa kassaprosessin valmiiksi vierailijana tai kirjautuneena käyttäjänä. Jos asiakas kirjautuu sisään, tilin tiedot, kuten tallennetut toimitusosoitteet ja tallennetun luottokortin tiedot, haetaan automaattisesti.

### <a name="order-summary"></a>Tilauksen yhteenveto

Kassaprosessi näyttää ostoskorin rivinimikkeiden yhteenvedon. Asiakas voi tarkistaa tilauksen ennen tilauksen tekemistä. Rivinimikkeitä ei voi muokata kassatyönkulun aikana. Näkyvissä on kuitenkin linkki ostoskoriin siltä varalta, että asiakas haluaa siirtyä takaisin ja muokata rivinimikkeitä.

Kun asiakas antaa toimitus- ja laskutustiedot, tilauksen yhteenvetoon päivittyy summa kanta-asiakkuuspisteiden, lahjakorttien ja muiden maksutapojen huomioimisen jälkeen.

### <a name="order-confirmation-and-email"></a>Tilausvahvistus ja sähköposti

Kun asiakas tekee tilauksen, hänelle annetaan vahvistusnumero. Tässä vaiheessa maksu on hyväksytty, mutta sitä ei ole veloitettu. Maksu veloitetaan vasta, kun tilaus on täytetty (eli kun se on joko lähetetty tai noudettu).

Tilauksen luomisen jälkeen asiakkaalle lähetetään tilausvahvistussähköpostiviesti.

Lisätietoja kassasivun muokkaamisesta on kohdassa [Kassamoduulin lisääminen sivulle](add-checkout-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Aloitussivun yleiskatsaus](quick-tour-home-page.md)

[Tuotetietosivujen yleiskatsaus](quick-tour-pdp.md)

[Tilinhallintasivujen yleiskatsaus](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
