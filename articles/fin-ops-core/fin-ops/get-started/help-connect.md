---
title: Talous- ja toimintosovellusten ohjekokemuksen määrittäminen
description: Tässä artikkelissa käsitellään joidenkin Microsoft Dynamics 365 -sovellusten ohjejärjestelmän osista.
author: margoc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f5d73075d118079ccb0616fbd1c5e1a8e00424
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123621"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Talous- ja toimintosovellusten ohjekokemuksen määrittäminen

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Tässä artikkelissa on talous- ja toimintosovellusten, kuten Microsoft Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin, Dynamics 365 Commercen ja Dynamics 365 Human Resourcesin, ohjejärjestelmän osien yleiskatsaus. Artikkelissa käsitellään myös kyseisten osien yhdistämistä ja annetaan yhteenveto mukautetun ohjeen luontiprosessista.

## <a name="help-architecture"></a>Ohjearkkitehtuuri

Talous- ja toimintosovellukset sisältävät käsitteellisiä yleiskatsauksia ja muita aiheita, jotka on julkaistu [Microsoft Dynamics 365 -ohjeet](/dynamics365/) -sivustossa. Tätä sisältöä voidaan sitten käyttöön tuotteen **Ohje**-ruudussa. Seuraavassa kuvassa on osa ohjejärjestelmästä.

[![Ohjearkkitehtuuri.](./media/help-architecture.png)](./media/help-architecture.png)

Tuotteen ohjejärjestelmä hakee artikkeleita docs.microsoft.comista ja muista yhdistetyistä sivustoista. Se hakee myös liiketoimintaprosessien mallintajaan Microsoft Dynamics Lifecycle Servicesissä (LCS) tallennetuista tehtäväoppaista.

## <a name="adding-task-guides"></a>Tehtäväoppaiden lisääminen

> [!NOTE]
> **Tehtäväoppaat**-välilehteä ei ole tällä hetkellä Human Resourcesissa tai Commercessa. <!--We are currently working to enable this functionality in a future release.--> Perustoimintoja koskevat Human Resourcesin aloituskokemuksen tehtäväoppaat ovat kuitenkin edelleen käytettävissä. Sekä Human Resourcesin että Commercen menettelyohjeet ovat käytettävissä [Microsoft Dynamics 365 -ohjeet](/dynamics365/) -sivustossa.

Järjestelmänvalvojat voivat määrittää **Järjestelmän parametrit** -sivulla käyttöönottoon soveltuvien tehtäväopaskirjastojen käyttöoikeudet.

> [!NOTE]
> - Ohjeen määrittämistä varten kirjauduttava tilille sinä vuokraajana, jossa sovellus on otettu käyttöön.
> - LCS-kirjastoon ei voi muodostaa yhteyttä sovelluksen siitä esiintymästä, jota käytetään paikallisella virtuaalikiintolevyllä (VHD).

[![Järjestelmäparametrit-lomake ja ohjeen asetukset.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Ratkaisun tehtäväoppaiden määrittämisohjeet ovat **Järjestelmän parametrit** -sivulla.

> [!IMPORTANT]
> Kun avaat **Ohje**-välilehden ensimmäisen kerran, sinun on muodostettava yhteys Lifecycle Services -palveluun. Valitse lomakkeen keskellä oleva linkki, odota yhteyden muodostumista, sulje valintaikkuna ja hae **Järjestelmäparametrit**-sivu valitsemalla **OK**.
>
> [![Muodosta yhteys LCS:ään](./media/connect-to-lcs-crop-1024x365.png "Yhteyden muodostaminen LCS:ään")](./media/connect-to-lcs-crop.png)

1. Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.
2. Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.
3. Määritä BPM-kirjastojen näyttöjärjestys. Näyttöjärjestys määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät **Ohje**-sivulla.

Kun olet suorittanut nämä vaiheet, voit avata **ohjeruudun** ja valita **Tehtäväoppaat**-välilehden, jolla on näkyvissä on avointa talous- ja toimintosovellusten sivua käsitteleviä tehtäväoppaita. Jos tehtävän ohjauksia ei löydy, tarkenna hakua avainsanoilla.

### <a name="showing-translated-task-guides"></a>Käännettyjen tehtäväoppaiden näyttäminen

Käännetyt tehtäväoppaat julkaistiin ensimmäisen kerran toukokuun 2016 yhdistetyssä APQC-kirjastossa ja käytön aloituskirjastossa. Lokalisoidun tehtäväoppaan ohjeen katsominen edellyttää, että Dynamics 365 -ratkaisu on yhdistetty toukokuun 2016 kirjastoon. Käyttäjät voivat muuttaa kielen, jota käytetään avautuvassa tehtäväoppaassa, muuttamalla kieliasetuksia kohdassa **Asetukset** &gt; **Asetukset**.

> [!NOTE]
> Vaikka useita tehtäväoppaita on käännetty, tehtäväoppaiden nimet eivät näy tällä hetkellä asiakasohjelmassa. Lisäksi vain helmikuussa 2016 julkaistujen tehtäväoppaiden käännökset ovat saatavana toukokuun 2016 kirjastossa. Microsoft julkaisee lisää käännöksiä sisältävän päivitetyn kirjaston.
>
> - Jos tehtäväopas on käännetty, tehtäväopas avautuu valitsemallasi kielellä.
> - Jos tehtäväopasta ei ole vielä käännetty, vain osa tekstistä (ohjausobjektien teksti) näkyy valitun kielisenä.

## <a name="adding-custom-help"></a>Mukautetun ohjeen lisääminen

Voit luoda tehtäväoppaiden avulla mukautetun ohjeen tai yhdistää mukautetun Ohje-sivuston **Ohje**-ruutuun.

### <a name="create-custom-help-by-using-task-guides"></a>Mukautetun ohjeen luominen tehtäväoppaiden avulla

Voit luoda tuettujen sovellusten oman mukautetun ohjeen luomalla toteutusta vastaavia tehtävätallenteita ja tallentamalla ne sitten LCS:n liiketoimintaprosessien kirjastoon. Human Resourcesiin ei voi luoda mukautettuja tehtäväoppaita.

Kumppanit voivat puolestaan siirtää kirjaston yrityskirjastoon ja sisällyttää sen ratkaisuun, jos se halutaan asiakkaiden käyttöön. Voit myös kopioida yhdistetyn APQC-kirjaston sekä avata tehtävätallenteet kopioissa, muokata niitä ja tallentaa sitten muutetut tallenteet. Lisätietoja on kohdassa [Tehtävän tallennustoiminnon resurssit](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Yhdistäminen mukautettuun ohjesivustoon

Talous- ja toimintosovelluksia käytetään vain harvoin sellaisenaan. Ratkaisu sen mukautetaan ja laajennetaan organisaation tarpeita vastaavaksi. Myös ohjekokemusta voi mukauttaa ja laajentaa. Mukautetun ohjeen voi esimerkiksi lisätä tuotteen **Ohje**-ruutuun.

Microsoftilla on työkalut, joilla mukautetun ohjeen voi ottaa käyttöön **Ohje**-ruudussa ja yhdistää siihen. Lisätietoja **Ohje**-ruutuun yhdistetyn mukautetun ohjeratkaisun määrittämisestä on kohdassa [Mukautetun ohjeen yleiskatsaus](../../dev-itpro/help/custom-help-overview.md).

Jos haluat tehdä Microsoftin kanssa yhteistyötä ohjeen mukauttamistyökalujen ja -prosessien osalta, täytä lomake osoitteessa [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Lisätietoja

[Ohjejärjestelmä](help-overview.md)  
[Mukautetun ohjeen yleiskatsaus](../../dev-itpro/help/custom-help-overview.md)  
[Tehtävän tallennustoiminnon resurssit](../../dev-itpro/user-interface/task-recorder.md)  
[Dokumentaation tai koulutuksen luominen tehtävien tallennustoiminnolla](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Mukautetun ohjeen GitHub-säilö](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

