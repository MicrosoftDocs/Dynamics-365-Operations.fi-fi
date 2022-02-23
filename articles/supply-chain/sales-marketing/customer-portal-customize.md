---
title: Asiakasportaalin mukauttaminen ja käyttäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka asiakasportaalia mukautetaan sen jälkeen, kun se on lisätty järjestelmään.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7849f354817f189bf7c844bbe2944f94c8fffe83
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527360"
---
# <a name="customize-and-use-the-customer-portal"></a>Asiakasportaalin mukauttaminen ja käyttäminen

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa esitellään eri sivut, jotka ovat valmiina käytettävissä asiakasportaalissa. Siinä selitetään, mitä sivut tekevät ja miten niitä voi mukauttaa.

Asiakasportaali tarjoaa joitakin valmiita verkkosivuja ja toimintoja. Seuraavassa sivustokartassa on yleiskatsaus kyseisistä verkkosivuista ja toiminnoista sekä tehtävistä, jotka voivat suorittaa toimenpiteet.

![Asiakkaan portaalisivuston sivustokartta](media/customer-portal-site-map.png "Asiakkaan portaalisivuston sivustokartta")

## <a name="typical-customizations"></a>Tyypilliset mukautukset

Seuraavissa ohjeaiheissa on tietoja Power Apps -portaalien perustoiminnoista ja portaalien mukauttamisesta:

- [Mallien käsitteleminen](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – Tämä ohjeaihe sisältää yleiskatsauksen Power Apps -portaalien toiminnasta ja siitä, miten voit tehdä portaalien yksinkertaisia mukautuksia.
- [Portaalin sisällönhallinta](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – Tässä ohjeaiheessa kerrotaan, kuinka voit hallita ja mukauttaa portaalissasi näkyvää sisältöä.
- [Muokkaa CSS:tä](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – Tämän ohjeaiheen avulla voit tehdä monimutkaisempia mukautuksia portaalin käyttöliittymään.
- [Luo portaaliin teema](https://docs.microsoft.com/dynamics365/portals/create-theme) – Tämän ohjeaiheen avulla voit luoda portaalin käyttöliittymän teeman.
- [Luo ja näytä portaalin sisältöä helposti](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – Tämän ohjeaiheen avulla voit hallita portaalissa käytössä olevia tietoja ja entiteettejä.
- [Yhteyshenkilön määrittäminen käytettäväksi portaalissa](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – Tässä ohjeaiheessa kerrotaan, kuinka käyttäjärooleja luodaan ja mukautetaan sekä kuinka suojaus ja todennus toimivat Power Apps -portaaleissa.
- [Yksikkölomakkeiden ja portaalien verkkolomakkeiden huomautusten määrittäminen](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – Tässä ohjeaiheessa kerrotaan, kuinka voit lisätä portaaliin asiakirjoja ja lisätallennustilaa.
- [Portaalin verkkosivuston virheenkäsittely](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – Tässä ohjeaiheessa kerrotaan, kuinka portaalin virhelokeja voidaan tarkastella ja tallentaa Microsoft Azure -Blob-objektisäilötilille.

## <a name="customize-the-order-creation-process"></a>Tilauksen luomisprosessin mukauttaminen

Kun käyttäjä lähettää tilauksen asiakasportaalin kautta, tilaus synkronoidaan automaattisesti vastaavaan Dynamics 365 Supply Chain Management -ympäristöön. Koska käyttäjä on ulkopuolinen asiakas, jotkin pakolliset tiedot on tarkoituksellisesti piilotettu häneltä. Nämä tiedot täytetään automaattisesti, kun lomake lähetetään.

Tässä osassa näkyy, miten yhteyshenkilöt on määritettävä virheiden välttämiseksi. Siinä selitetään kentät, jotka määritetään automaattisesti, ja voit muokata kenttien arvoa, jos niitä on.

### <a name="the-out-of-box-order-creation-process"></a>Valmis tilauksen luomisprosessi

Tässä ovat vakiovaiheet tilauksen lähettämiselle asiakasportaalista.

1. Avaa ohjattu **Luo tilaus** -toiminto valitsemalla aloitussivulla **Luo tilaus** -ohjattu toiminto.
1. Määritä **Tilauksen tiedot** -sivulla seuraavat kentät:

    - **Pyydetty vastaanottopäivä** – Määritä toimituspäivämäärä.
    - **Toimitusosoite** – Syötä osoite, johon tilaus toimitetaan.
    - **Yritys** – Valitse asiakasyrityksen nimi. Tämä kenttä määritetään automaattisesti muille kuin järjestelmänvalvoja-käyttäjille.
    - **Hankintanumero** – Syötä tilauksen tilausnumero. Tämä kenttä ei ole pakollinen.
    - **Toimita maahan/alueelle** – Määritä maa tai alue, johon nimikkeet toimitetaan. Tämä kenttä määritetään automaattisesti muille kuin järjestelmänvalvoja-käyttäjille.

    ![Tilauksen tiedot -sivu](media/customer-portal-order-information.png "Tilauksen tiedot -sivu")

1. Valitse **Seuraava**.
1. Valitse **Nimikkeet**-sivulla **Lisää nimike**.

    ![Tuotesivu](media/customer-portal-items.png "Tuotesivu")

1. **Tuotetieto**-valintaikkunassa kuvaillaan seuraavat kentät:

    - **Tuotteen nimi** – Etsi ja valitse tilaukseen lisättävä tuote.
    - **Määrä** – Syötä valitun tuotteen määrä.
    - **Yksikkö** – Määritä mittayksikkö (esimerkiksi **kpl**, **kg** tai **laatikko**).
    - **Arvioitu nettosumma** – Arvo lasketaan nimikkeen arvioituna hintana valitun yksikkömäärän mukaan.

    ![Tuotetieto-valintaikkuna](media/customer-portal-item-information.png "Tuotetieto-valintaikkuna")

1. Lisää nimike tilaukseen valitsemalla **Lähetä**.
1. Toista vaiheet 4 - 6, kunnes olet lisännyt kaikki tilattavat nimikkeet.
1. Kun olet lisännyt haluamasi nimikkeet, valitse **Nimikkeet**-sivulta **Seuraava**.
1. **Tilauksen tiedot** -sivulla on tilauksen yhteenveto. Tarkista tilauksen sisältö ja toimitustiedot. Jos kaikki näyttää oikealta, lähetä tilaus valitsemalla **Lähetä**.

    ![Tilauksen tiedot -sivu](media/customer-portal-order-submit.png "Tilauksen tiedot -sivu")

### <a name="standard-data-setup"></a>Tietojen vakioasetus

Jotta käyttäjäkokemus olisi sujuva, asiakasportaali täyttää automaattisesti useiden pakollisten kenttien arvot. Nämä arvot perustuvat tilauksen lähettäneen asiakkaan yhteyshenkilötietueen tietoihin.

Seuraavien pakollisten kenttien arvot on määritettävä jokaiselle sellaiselle [yhteystietotietueelle](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts), joka kuuluu asiakkaalle, joka käyttää asiakasportaalia tilausten lähettämiseen. Muussa tapauksessa tapahtuu virheitä.

- **Yritys** – Yritys, joka omistaa tilauksen
- **Potentiaalinen asiakas** – Tilaukseen liittyvä asiakastili
- **Hinnasto** – Asiakkaan mukautettu hinnasto
- **Valuutta** – Hinnan valuutta
- **Toimita maahan/alueelle** – Maa tai alue, johon nimikkeet toimitetaan

Seuraavat kentät määritetään automaattisesti myyntitilauskohteelle:

- **Kieli** – Tilauksen kieli (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)
- **Toimita maahan/alueelle** – Maa tai alue, johon nimikkeet toimitetaan (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)
- **Yhteyshenkilö** – Käyttäjä, jolle voidaan ottaa yhteyttä tilauksen lisätietoja varten (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)
- **Yritys** – Yritys, johon tilaus kuuluu (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)
- **Potentiaalinen asiakas** – Tilaukseen liittyvä asiakastili (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)
- **Laskutusasiakas** – Tilauksen laskutustili (Oletusarvo on potentiaalinen asiakas yhteyshenkilötietueesta.)
- **Myyntitilauksen nimi** – Myyntitilauksen nimi (oletusarvo on **myyntitilaus**.)
- **Valuutta** – Hinnan valuutta (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)
- **Hinnasto** – Asiakkaan mukautettu hinnasto (Oletusarvon mukaan arvo haetaan yhteyshenkilötietueesta.)
- **Toimitusosoitteen kuvaus** – Myyntitilauksen toimitusosoite (oletusarvo on **Toimitusosoitteen kuvaus**.)

### <a name="modify-the-order-creation-process"></a>Tilauksen luomisprosessin muokkaaminen

Voit muokata asiakasportaalin ulkoasua ja käyttöliittymää vapaasti, jos et muuta perustilauksen luomisprosessia. Jos haluat muuttaa tilauksen luomisprosessia, on joitakin seikkoja, jotka on syytä pitää mielessä.

Älä poista seuraavia kenttiä myyntitilausyksiköstä Common Data Servicessä, koska niitä tarvitaan myyntitilauksen luomiseen kaksoiskirjoituksessa:

- **Yritys** – Yritys, joka omistaa tilauksen
- **Nimi** – Myyntitilauksen nimi
- **Valuutta** – Hinnan valuutta
- **Hinnasto** – Asiakkaan mukautettu hinnasto
- **Toimita maahan/alueelle** – Maa tai alue, johon nimikkeet toimitetaan
- **Potentiaalinen asiakas** – Tilaukseen liittyvä asiakastili
- **Kieli** – Tilauksen kieli (yleensä tämä kieli on mahdollisen asiakkaan kieli.)
- **Toimitusosoitteen kuvaus** – Myyntitilauksen toimitusosoite

Nimikkeille tarvitaan seuraavat kentät:

- **Tuote** – Tilattava tuote
- **Määrä** – Valitun tuotteen määrä
- **Yksikkö** – Mittayksikkö (esimerkiksi **kpl**, **kg** tai **laatikko**)
- **Lähetys maa/alue** – Toimitusmaa tai -alue
- **Toimitusosoitteen kuvaus** – Tilauksen toimitusosoite

Sinun on varmistettava, että asiakasportaali jotenkin lähettää arvot kaikille näille kentille.

Jos haluat lisätä sivulle kenttiä tai poistaa kenttiä, lisätietoja on kohdassa [Pikaluonnin lomakkeiden luominen tai muokkaaminen selkeytettyä tietojen syöttökokemusta varten](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Jos haluat muuttaa tapaa, jolla kentät on määritetty valmiiksi ja kuinka arvot määritetään, kun sivu tallennetaan, tutustu seuraaviin Power Apps -portaalin käyttöohjeissa oleviin tietoihin:

- [Täytä kenttä valmiiksi](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Aseta arvo tallennettaessa](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Kotisivun mukauttaminen

Kaikki asiakasportaalin ohjausobjektit ovat sisäänrakennettuja Power Apps -portaalien ohjausobjekteja. Voit mukauttaa niitä noudattamalla ohjeita, jotka liittyvät [sivun luomiseen](https://docs.microsoft.com/powerapps/maker/portals/compose-page) Power Apps -portaalien dokumentaatiossa.

Vain asiakasportaalin mallipohjaan sisältyvää mukautettua ohjausobjektia käytetään luotaessa ruutuja kotisivulle.

![Kotisivun ruudut](media/customer-portal-home-page-tiles.png "Kotisivun ruudut")

Voit muokata ruutuja seuraavasti.

1. Avaa [Portaalin hallintasovellus](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivumallit**.

    ![Portaalinhallinnan siirtymisruutu](media/customer-portal-nav.png "Portaalinhallinnan siirtymisruutu")

1. Valitse sivupohja, jonka nimi on **Koti**.
1. Avaa sivun lähdekoodi valitsemalla **Verkkomalli**-kentässä **Koti**-linkki.

    ![Verkkomallin kenttä](media/customer-portal-web-template.png "Verkkomallin kenttä")

1. Sinun pitäisi nyt nähdä koko kotisivun lähdekoodi ja voi muokata sitä kuin tarvitset.

## <a name="resources"></a>Resurssit

Lisätietoja asiakasportaalin määrittämisestä ja mukauttamisesta on seuraavissa resursseissa:

- [Power Apps -portaalit -dokumentaatio](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Kaksoiskirjoituksen dokumentointi](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Tietoja portaalin elinkaaresta](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Portaalin päivittäminen](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Portaalin konfiguraation siirtäminen](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Ratkaisun elinkaaren hallinta: Dynamics 365 for Customer Engagement -sovellukset](https://www.microsoft.com/download/details.aspx?id=57777)
