---
title: Linkittämättömien palautusten käsitteleminen Adyenin Dynamics 365 Commerce Payment Connectorin avulla
description: Tässä artikkelissa kuvataan, miten linkittämättömät hyvitykset toimivat, kun Adyenin Microsoft Dynamics 365 Payment Connectoria käytetään.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 634b30de7adbfb0c316fe14456581ea8eb89d070
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885194"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Linkittämättömien palautusten käsitteleminen Adyenin Dynamics 365 Commerce Payment Connectorin avulla

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten linkittämättömät hyvitykset toimivat, kun [Adyenin Microsoft Dynamics 365 Payment Connectoria](adyen-connector.md) käytetään. Siinä myös käsitellään hyvitysten käsittely uutta maksutapaa vastaan myyntipisteessä (POS) tai soittokeskuksessa.

Adyenin Dynamics 365 Payment Connector tukee hyvitysten käsittelykykyä käyttäen eri maksutapaa kuin alkuperäisessä tapahtumassa on käytetty. Vaikka suosittelemme, että käytät [linkitettyjä hyvityksiä](linked-refunds.md) ja käsittelet hyvityksen annettua alkuperäistä maksumenetelmää vastaan, joissakin tilanteissa on käytettävä eri maksutapaa palautuksessa. Esimerkiksi alkuperäisessä maksussa käytetty kortti voi olla vanhentunut tai hävinnyt tai käyttäjä on voinut peruuttaa sen.

## <a name="prerequisites"></a>Edellytykset

Seuraavat edellytykset on täytettävä, ennen kuin Adyenin Dynamics 365 Payment Connector voi käsitellä linkittämättömät hyvitykset:

- [Maksutapojen](../payment-methods.md) määrittäminen.
- Määritä [monikanavaiset maksut](../omni-channel-payments.md).

## <a name="additional-configuration"></a>Lisämääritys

Adyenin Dynamics 365 Payment Connector tarjoaa käyttövalmiina kaikki seuraavassa osassa kuvatut tuetut hyvitysskenaariot. Jos asiakas ei käytä Adyenin Dynamics 365 Payment Connectorin valmista toteutusta, asiakkaan on määritettävä liitin, joka tukee luottokorttien tunnuksien määritystä.

## <a name="supported-refund-scenarios"></a>Tuetut hyvitysskenaariot

Dynamics 365 Commerce tukee sellaisten tapahtumien hyvityksiä, jotka on aiemmin hyväksytty ja vahvistettu. Hyvitykset voivat sisältää tapahtuman joko täyden hyvityksen tai osittaisen hyvityksen. Hyvitykset eivät voi ylittää alkuperäistä maksun varmennussummaa. Linkittämätöntä hyvitystä tuetaan vain myyntipisteessä ja soittokeskuksessa.

## <a name="enable-unlinked-refunds-functionality"></a>Linkittämättömien palautusten ominaisuuden ottaminen käyttöön

Jos haluat ottaa käyttöön linkittämättömien hyvitysten toiminnon Commerce headquarters -sovelluksessa, toimi seuraavasti.

1. Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan jaetut parametrit**.
1. Aseta **monikanavamaksujen** -välilehdessä **Käytä monikanavamaksuja** -asetukseksi **Kyllä**.

### <a name="supported-payment-method-variants"></a>Tuetut maksutapojen variantit

Seuraavat maksutavan versiot tukevat linkittämätöntä palautusta käyttövalmiina:

- Kortit
- Lompakko

Kaikki maksutavan variantit eivät tue linkittämätöntä palautusta. Seuraavassa taulukossa on luettelo tavallisista maksutavoista sekä kunkin menetelmän linkitettyjen ja linkittämättömien palautusten tuetut ominaisuudet.

| Maksutapa        | Linkitetty palautus | Linkittämätön palautus |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Kyllä           | Kyllä             |
| amexconsumer          | Kyllä           | Kyllä             |
| amexcorporate         | Kyllä           | Kyllä             |
| amexdebit             | Kyllä           | Kyllä             |
| amexprepaid           | Kyllä           | Kyllä             |
| amexprepaidreloadable | Kyllä           | Kyllä             |
| amexsmallbusiness     | Kyllä           | Kyllä             |
| discover              | Kyllä           | Kyllä             |
| maestro               | Kyllä           | Kyllä             |
| maestrouk             | Kyllä           | Kyllä             |
| mc                    | Kyllä           | Kyllä             |
| mcalphabankbonus      | Kyllä           | Kyllä             |
| mcprepaidanonymous    | Kyllä           | Kyllä             |
| visa                  | Kyllä           | Kyllä             |
| visaalphabankbonus    | Kyllä           | Kyllä             |
| visacheckout          | Kyllä           | Kyllä             |
| visadankort           | Kyllä           | Kyllä             |
| visahipotecario       | Kyllä           | Kyllä             |
| visasaraivacard       | Kyllä           | Kyllä             |
| vpay                  | Kyllä           | Kyllä             |
| givex                 | **Ei**        | Kyllä             |
| svs                   | **Ei**        | Kyllä             |
| cup                   | Kyllä           | Kyllä             |
| diners                | Kyllä           | Kyllä             |
| interac               | **Ei**        | Kyllä             |
| jcb                   | Kyllä           | Kyllä             |
| jcb_applepay          | Kyllä           | Kyllä             |
| unionpay              | Kyllä           | Kyllä             |

### <a name="process-an-unlinked-refund-in-pos"></a>Linkittämättömän hyvityksen käsitteleminen myyntipisteessä

Asiakas palauttaa nimikkeen myyntipisteen kassaan palautusten sallitun kauden aikana ja asiakkaalla on voimassa oleva kuitti. Palautuksen käsittelyn aikana **Palauta maksu** -valintaikkunassa on **Valitse maksutapa** -vaihtoehto. Kassanhoitaja voi sitten valita maksutavan hyvitysten tuetuista maksutavoista (kortit ja rahat).

### <a name="process-an-unlinked-refund-in-call-center"></a>Linkittämättömän hyvityksen käsitteleminen soittokeskuksessa

Kun linkittämätön hyvitys käsitellään tilauksen perusteella soittokeskuksessa, soittokeskuksen työntekijä valitsee maksutavan, joka eroaa alkuperäisestä maksutavasta. Järjestelmä pyytää työntekijää määrittämään järjestelmänvalvojan ohituksen henkilökohtaisen PIN-tunnusnumeron. PIN-koodi on pakollinen, ennen kuin hyvityksen voi käsitellä eri maksutapaan.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Järjestelmänvalvojan ohituksen PIN-koodin määrittäminen puhelinkeskusta varten

Jos haluat määrittää järjestelmänvalvojan ohituksen PIN-koodin Commerce headquarters -puhelinkeskuksessa, noudata seuraavia ohjeita.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan määritys \> Soittokeskuksen asetukset** tai etsi "ohitusoikeudet".
1. Valitse rooli, jolle linkittämättömän hyvityksen käsittelyoikeudet sallitaan.
1. Määritä **Palautukset**-pikavälilehdessä **Salli vaihtoehtoinen maksu** -asetuksen arvoksi **Kyllä**.

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Payment Connector Adyenia varten](adyen-connector.md)

[Aiemmin hyväksyttyjen ja vahvistettujen tapahtumien linkitetyt hyvitykset](linked-refunds.md)
