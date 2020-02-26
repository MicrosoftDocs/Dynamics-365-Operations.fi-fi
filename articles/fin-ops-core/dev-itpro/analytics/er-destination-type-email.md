---
title: Sähköpostin ER-kohteen tyyppi
description: Tässä ohjeaiheessa annetaan tietoja siitä, miten kullekin lähteviä asiakirjoja luomaan määritetty sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentin sähköpostikohde määritetään.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019746"
---
# <a name="EmailDestinationType">Sähköpostikohde</a>

[!include [banner](../includes/banner.md)]

Voit määrittää sähköpostikohteen kullekin lähteviä asiakirjoja luomaan määritetylle sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentille. Luotu asiakirja toimitetaan sähköpostiviestin liitteenä kohdeasetuksen perusteella.

Lähetä tulostetiedosto sähköpostitse valitsemalla **Käytössä**-asetukseksi **Kyllä**. Kun tämä asetus on otettu käyttöön, voit muokata sähköpostin aihetta ja määrittää sähköpostin vastaanottajat. Voit määrittää vakiotekstit sähköpostiviestin aiheelle ja perustekstille tai voit ER-[kaavojen ](er-formula-language.md) avulla dynaamisesti luoda sähköpostitekstejä. 

Voit määrittää sähköisen raportoinnin sähköpostiosoitteet kahdella tavalla. Määritys voidaan suorittaa loppuun samalla tavalla kuin Tulostuksenhallinta-ominaisuus suorittaa sen loppuun. Voit myös ratkaista sähköpostiosoitteen käyttämällä suoraa viitettä ER-määritykseen kaavan kautta.

[![Sähköpostikohteen käyttöönotto](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Sähköpostiosoitteen tyyppi

Kun valitset **Muokkaa** kentässä **Vastaanottaja** tai **Kopio**, **Sähköpostin vastaanottaja** -valintaikkuna tulee näyttöön. Voit sitten valita minkä tyyppistä sähköpostiosoitetta haluat käyttää. Tällä hetkellä tuetaan sähköpostityyppejä **Määrityssähköposti** ja **Tulostuksenhallinta**.

[![Valitse sähköpostityyppi](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Tulostuksenhallinta

Jos valitset **Tulostuksenhallinta** -sähköpostityypin, voit syöttää kiinteät sähköpostiosoitteet **Vastaanottaja**-kenttään. 

[![Kiinteiden sähköpostiosoitteiden määritys](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Jos haluat käyttää muita kuin kiinteitä sähköpostiosoitteita, tiedostokohteen sähköpostin lähdetyyppi on valittava. Seuraavia arvoja tuetaan: **Asiakas**, **Toimittaja**, **Prospekti**, **Yhteyshenkilö**, **Kilpailija**, **Työntekijä**, **Hakija**, **Mahdollinen toimittaja** ja **Ei-sallittu toimittaja**. Kun olet valinnut sähköpostin lähdetyypin, käytä **Sähköpostin lähdetili** -kentän vieressä olevaa painiketta, jos haluat avata **Reseptien suunnittelu** -lomakkeen. Voit käyttää tätä muotoa liittääksesi kaavan, joka palautta suorituksen aikana valitun lähdetyypin **osapuolen tilin** käsitellystä asiakirjasta sähköpostikohteeseen.

[![Sähköpostilähdetilin määritys](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Kaavat ovat ER-määrityskohtaisia. Kirjoita **Kaava**-kenttään asiakirjakohtainen viittaus asiakas- tai toimittajaosapuolen tyyppiin. Kirjoittamisen asemesta voit etsiä tietolähdesolmun, joka vastaa asiakkaan tai toimittajan tiliä, ja päivittää kaavan valitsemalla **Lisää tietolähde**. Jos käytössä on esimerkiksi **ISO 20022 Tilisiirto** -määritys, toimittajatiliä vastaava solmu on `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Jos annat merkkijonoarvon, kuten `"DE-001"`, ja tallennat kaavan, toimittajan **DE-001** yhteyshenkilölle lähetetään sähköpostiviesti.


[![ER-kaavan suunnittelusivu](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![Sähköpostilähdetilin määritys](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Määrityssähköposti

Käytä tätä sähköpostityyppiä, jos käyttämässäsi määrityksessä tietolähteissä solmu, joka palauttaa **sähköpostiosoitteen**. Voit käyttää reseptien suunnittelun tietolähteitä ja funktioita saadaksesi oikein muotoillun sähköpostiosoitteen. Jos käytössä on esimerkiksi **ISO 20022 Tilisiirto** -määritys, toimittajan yhteyshenkilön sähköpostiositetta vastaava solmu on `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Sähköpostiositelähteen määritys](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)
- [Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)
