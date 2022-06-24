---
title: Tulostimen ER-kohteen tyyppi
description: Tässä artikkelissa käsitellään tulostinkohteen määrittämistä sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-osalla.
author: NickSelin
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 826455d0901a45ef26755fd323ee2a2737b5eec0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845567"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Tulostinkohde

[!include [banner](../includes/banner.md)]

Voit lähettää luodun asiakirjan suoraan verkkotulostimeen suoraa tulostusta varten.

## <a name="prerequisites"></a>Edellytykset

Ennen aloittamista sinun on asennettava ja määritettävä asiakirjan reititysagentti ja rekisteröitävä sitten verkkotulostimet. Lisätietoja on kohdassa [Verkkotulostuksen käyttöönotto asentamalla asiakirjan reititysagentti](./install-document-routing-agent.md)

## <a name="make-the-printer-destination-available"></a>Tulostinkohteen käytettäväksi asettaminen

Jos haluat, että **Tulostin**-kohde on käytettävissä Microsoft Dynamics 365 Financen kulloisessakin esiintymässä, siirry **Ominaisuuksien hallinta** -työtilaan ja ota seuraavat ominaisuudet käyttöön tässä järjestyksessä:

1. Muunna sähköisen raportoinnin lähtevät asiakirjat Microsoft Office -muodoista PDF-muotoon
2. Asiakirjareitityksen agentti lähtevien asiakirjojen sähköisen raportoinnin kohteena

[![ER-tulostinkohteen toiminnon käyttöönotto ominaisuuksien hallinnassa.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Soveltuvuus

#### <a name="pdf-printing"></a>PDF-tulostaminen

Finance-versiota 10.0.18 aiemmissa versioissa **Tulostin**-kohde voidaan määrittää vain tiedostokomponenteille, joita käytetään tulosteen luomiseen joko tulostettavassa PDF-muodossa (**PDF Mergerin** tai **PDF-tiedoston** muotoelementit) tai Microsoft Office Excel- ja Word-muodossa (**Excel**-tiedosto). Kun tuloste luodaan PDF-muodossa, se lähetetään tulostimeen. Kun tuloste luodaan Office-muodossa käyttämällä **Excel-tiedosto**-muotoelementtiä, se muunnetaan automaattisesti PDF-muotoon ja lähetetään sitten tulostimeen.

Versiosta 10.0.18 alkaen voit kuitenkin määrittää **Tulostin**-kohteen **Common File** -muotoelementille. Tätä muotoelementtiä käytetään yleensä joko TXT- tai XML-muotoiseen tulostukseen. Voit konfiguroida **Common file** -muotoelementin sisältävän ER-muodon juurimuotoelementiksi ja **binaarisisällön** muotoelementin sen ainoaksi sisäkkäiseksi elementiksi. Tässä tapauksessa **Common File** -muotoelementti tuottaa tuotoksen muodossa, joka määritetään **binaarisisällön** muotoelementille määritettävällä sidonnalla. Voit esimerkiksi määrittää tämän sidonnan [täyttämään](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) tämän elementin [asiakirjanhallinnan](../../fin-ops/organization-administration/configure-document-management.md) liitteen sisällöllä PDF- tai Office (Excel tai Word) -muodossa. Voit tulostaa tulosteen käyttämällä määritettyä **Tulostin**-kohdetta. 

> [!NOTE]
> Kun valitset **Common\\File**-muotoelementin **Tulostin**-kohteen konfiguroimiseksi, suunnittelun aikana ei voida taata, että valittu elementti tuottaa tuotoksen PDF-muodossa tai PDF-muotoon muunnettavassa muodossa. Näin saat seuraavan varoitussanoman: "Varmista, että valitun muotokomponentin luoma tulostus voidaan muuntaa PDF-tiedostomuotoon. Poista muussa tapauksessa Muunna PDF-tiedostoksi -vaihtoehto." Sinun on tehtävä vaiheita, jotka auttavat ehkäisemään suorituksenaikaiset ongelmat, kun suorituksen aikana tulostetaan muu kuin PDF-tiedosto tai muu kuin PDF-muotoon muunnettava tuloste. Jos haluat vastaanottaa tuotoksen Office (Excel tai Word) -muodossa, **Muunna PDF-muotoon** -vaihtoehto on valittava.
>
> Versiossa 10.0.26 ja sitä myöhemmissä versioissa **Muunna PDF-muotoon** -asetuksen käyttämiseksi sinun on valittava **PDF** konfiguroidun **Tulostin**-kohteen **Asiakirjan reititystyyppi** -parametria varten.

#### <a name="zpl-printing"></a>ZPL-tulostaminen

Versiossa 10.0.26 ja sitä myöhemmissä versioissa voit määrittää **Common\\File**-muotoelementin **Tulostin**-kohteen valitsemalla **Asiakirjan reititystyyppi** -parametriksi **ZPL**. Tässä tapauksessa **Muunna PDF-muotoon** -asetus ohitetaan suorituksen aikana ja TXT- tai XML-tuloste lähetetään suoraan valitulle tulostimelle [asiakirjan reititysagentin (DRA)](install-document-routing-agent.md) Zebra Programming Language (ZPL) -määrityksen avulla. Tämän toiminnon avulla voit tulostaa erilaisia etikettejä ER-muodolle, joka edustaa ZPL II -etikettiasettelua.

[![Tiedoston reititystyyppiparametrin määrittäminen Kohdeasetukset-valintaikkunassa.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Lisätietoja tästä ominaisuudesta on kohdassa [Suunnittele uusi ER-ratkaisu ZPL-etikettien tulostamista varten](er-design-zpl-labels.md).

### <a name="limitations"></a>Rajoitukset

**Tulostin**-kohdetta käytetään vain pilvikäyttöönotoissa.

### <a name="use-the-printer-destination"></a>Käytä tulostinkohdetta

1. Määritä **Käytössä** -asetuksen arvoksi **Kyllä**, jos haluat lähettää luodun tiedoston tulostimeen.
2. Valitse **Tulostimen nimi** -kentässä asianmukainen verkkotulostin.
3. Aseta **Tallenna tulostusarkistoon?** -asetuksen arvoksi **Kyllä**, jos haluat tallentaa luodun tulosteen tulostusarkistoon, jotta se voidaan tulostaa myös myöhemmin. Arkistoitu tuloste on myöhemmin käytettävissä kohdassa **Organisaation hallinta** \> **Kyselyt ja raportit** \> **Raporttiarkisto**.

[![Tulostinkohteen käyttö.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> **Muunna PDF-muotoon** -asetuksen ei tarvitse olla käytössä, kun määrität **Tulostin**-kohteen. PDF-muunnos tulostusta varten tapahtuu, vaikka asetus ei olisi käytössä.

Jos haluat käyttää tiettyä [sivun suuntaa](electronic-reporting-destinations.md#SelectPdfPageOrientation), kun tulostat lähtevän asiakirjan Excel-muodossa, **Muunna PDF-muotoon** -asetus on otettava käyttöön. Kun määrität **Muunna PDF:ksi** -asetukseksi **Kyllä**, **Sivun suunta** -kenttä on käytettävissä. **Sivun suunta** -kentästä voit valita haluamasi sivun suunnan.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
