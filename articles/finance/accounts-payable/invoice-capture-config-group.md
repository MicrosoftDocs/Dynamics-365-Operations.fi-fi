---
title: Invoice Capture -ratkaisun konfiguraatioryhmät
description: Tässä artikkelissa on yleistietoja Invoice Capture -ratkaisun konfiguraatioryhmistä.
author: sunfzam
ms.date: 09/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691167"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Invoice Capture -ratkaisun konfiguraatioryhmät

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Käyttäjät voivat hallita laskukenttäluetteloa ja yritysten manuaalisen tarkistuksen asetusta konfiguraatioryhmien avulla. Käyttäjät voivat määrittää laskumäärityksiä eri yrityksille ryhmissä. Kaikki saman konfiguraatioryhmän yritykset käyttävät samoja laskukenttiä ja manuaalisen tarkistuksen asetusta.

## <a name="manage-configuration-groups"></a>Konfiguraatioryhmien hallinta

Jos haluat hallita konfiguraatioryhmiä sovelluksen avulla, siirry **Asetus**-kohtaan ja valitse **Järjestelmäasetus \> Määritä konfiguraatioryhmien osa**.

**Määritä konfiguraatioryhmät** -sivun päävälilehdessä on luettelo määritetyistä konfiguraatioryhmistä. Sivulla näkyy myös oletuskonfiguraatioryhmä. Seuraavat toiminnot ovat käytettävissä kullekin konfiguraatioryhmälle:

- **Kopioi konfiguraatioryhmä** – Voit luoda uuden konfiguraatioryhmän kopioimalla aiemmin luodun ryhmän. Uudella ryhmällä on samat arvot kuin alkuperäisellä ryhmällä kaikissa muissa kentissä paitsi **Ryhmän nimi**- ja **Ryhmän kuvaus** -kentässä. Valitse konfiguraatioryhmän monistamisen jälkeen **OK**.
- **Poista konfiguraatioryhmät** – Voit poistaa konfiguraatioryhmän valitsemalla sen ja valitsemalla sitten **Poista**.

    > [!NOTE]
    > Oletuskonfiguraatioryhmää ei voi poistaa.

- **Muokkaa konfiguraatioryhmän tunnusta** – Jos haluat muokata konfiguraatioryhmän tunnusta, valitse **Ryhmän tunnus** -kenttä ja päivitä arvo. Ryhmän tunnuksessa ei saa olla välilyöntejä tai erikoismerkkejä, eikä se saa olla yli 20 merkkiä pitkä.

    > [!NOTE]
    > **Ryhmän tunnus** -kentän arvon voi päivittää vain kerran.

- **Muokkaa konfiguraatioryhmän kuvausta** – Jos haluat muokata konfiguraatioryhmän kuvausta, valitse **Kuvaus**-kenttä ja päivitä arvo.
- **Muuta manuaalista tarkistusasetusta** – Käyttäjät voivat päättää, onko lasku tarkistettava manuaalisesti. Voit muuttaa manuaalisen tarkistusasetuksen valitsemalla **Vaatii manuaalisen tarkistuksen** -vaihtoehdon. Käytettävissä ovat seuraavat asetukset:

    - **Aina manuaalinen tarkistus** – Valitse tämä vaihtoehto, jos konfiguraatioryhmän laskut on aina tarkistettava manuaalisesti.
    - **Virheet ja varoitukset** – Valitse tämä vaihtoehto, jos virhe- tai varoitussanomia sisältävät laskut on tarkistettava manuaalisesti.
    - **Virheet** – Valitse tämä vaihtoehto, jos virhesanomia sisältävät laskut on tarkistettava manuaalisesti.

- **Muuta luotettavuuspisteiden asetusta** – Luotettavuuspisteet ovat Invoice Capture -ratkaisun toimittamat metatiedot, joiden avulla tunnistettujen laskutietojen tarkkuus raportoidaan.. Mitä suuremmat pisteet saadaan, sitä tarkempia tunnistetut tiedot voivat olla. Konfiguraation avulla käyttäjät voivat määrittää, milloin manuaalinen tarkistus on tarpeen luotettavuuspisteiden perusteella. Käyttäjät voivat muuttaa laskujen luotettavuuspisteiden raja-arvoa. Voit päivittää luotettavuuspisteiden asetuksen valitsemalla **Luotettavuuspisteet**-kentän ja päivittämällä arvon.

    Luotettavuuspisteillä on seuraavat kaksi hälytystyyppiä:

    - **Varoitus** – Laskukenttiä, joiden luotettavuuspisteet ylittävät varoitusten raja-arvon, pidetään oikeina. Varoitusten raja-arvon on oltava suurempi kuin virheiden raja-arvo ja pienempi kuin 100.
    - **Virhe** – Laskukenttiä, joiden luotettavuuspisteet alittavat virheiden raja-arvon, pidetään virheellisinä. Virhesanomat näytetään käyttäjälle. Virheiden raja-arvon on oltava suurempi kuin 0 (nolla) tai pienempi kuin varoitusten raja-arvo. Varoitussanomat näytetään laskukentissä, joiden luotettavuuspisteiden määrä on varoitusten raja-arvon ja virheiden raja-arvon välillä.

- **Laskukenttien hallinta** – Käyttäjät voivat hallita laskukenttäluetteloa, joka näkyy rinnakkaisessa katseluohjelmassa. Valitse **Laskukenttien hallinta** -välilehdessä rataskuvake. Valitse lisättävät laskukentät ja valitse sitten **Tallenna**. Valitut kentät lisätään luetteloon. Jos haluat poistaa laskukentän luettelosta, valitse kentässä **Poista**.

### <a name="manage-file-filters-optional"></a>Tiedoston suodattimien hallinta (valinnainen)

Tiedoston suodattimien hallinnan avulla käyttäjät voivat määrittää lisäsuodattimia saapuville laskutiedostoille. Tiedostot, jotka eivät vastaa suodatusehtoja, vastaanotetaan ja näytetään **Vastaanotetut tiedostot** -luettelossa, mutta niissä näkyy tiedoston vahvistusvirheitä. Tämä toiminta on erilaista kuin kanavassa määritetyillä suodattimilla. Näissä suodattimissa tiedostoja, jotka eivät täytä ehtoja, ei vastaanoteta lainkaan. Käyttäjät voivat tarkistaa saapuvat tiedostot ja päättää, onko tiedosto kelvoton lasku. He voivan määrittää tiedoston vanhentuneeksi tai sisällyttää sen manuaalisesti tunnistusta ja sisällytystä varten siepatuissa laskuissa.

Kun Invoice Capture -ratkaisu on asennettu, määritetään oletustiedostosuodatin. Tämä on yleinen tiedostosuodatin. Jos haluat muuttaa suodatusasetuksia, voit päivittää oletussuodattimen. Jos kenttä on pakollinen, valitse **Pakollinen**. 

### <a name="accepted-file-size"></a>Hyväksytty tiedostokoko

Voit valita hyväksytyn tiedostokoon.

> [!NOTE]
> Tiedostoja, jotka ovat suurempia kuin 20 480 kilotavua (kt), ei tueta.

### <a name="supported-file-types"></a>Tuetut tiedostotyypit

Tällä hetkellä tuetaan seuraavia tiedostotyyppejä:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF
