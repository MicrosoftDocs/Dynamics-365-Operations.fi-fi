---
title: Maan tai alueen valitsinmoduuli
description: Tässä ohjeaiheessa käsitellään maan tai alueen valitsinmoduulia ja kuvataan, miten se määritetään Microsoft Dynamics 365 Commercessa.
author: stuharg
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 9c20e614053b7a79cf962990dbd13ca0f45d5a00
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551667"
---
# <a name="countryregion-picker-module"></a>Maan tai alueen valitsinmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään maan tai alueen valitsinmoduulia ja kuvataan, miten se määritetään Microsoft Dynamics 365 Commercessa.

Maan tai alueen valitsinmoduuli käyttää Dynamics 365 Commercen [maantieteellisen sijainnin tunnistuksen ja uudelleenohjauksen](geo-detection-redirection.md) oinaisuutta näyttääkseen suositeltuja sivustoja asiakkaille, jotka pyytävät sellaisen sähköisen kaupankäyntisivuston URL-osoitetta, joka ei liity heidän maahansa tai alueeseensa.

Esimerkiksi Kanadassa oleva asiakas voi pyytää sellaisen sivun URL-osoitetta, joka liittyy johonkin muuhun maahan kuin Kanadaan. Tällöin maan tai alueen valitsinmoduuli näyttää valintaikkunan, joka suosittelee Kanadaan liittyvien sivustojen URL-osoitteita. 

## <a name="how-it-works"></a>Näin se toimii

Kun maantieteellinen paikannus ja uudelleenohjaus on otettu käyttöön sivustossa ja asiakas pyytää sivuston URL-osoitetta, asiakkaalle havaittua maata ja hänen pyytämänsä URL-osoitetta käytetään määrittämään, onko URL-osoite kohdistettu siihen maahan, jossa asiakas on. URL-osoitteiden ja maiden välinen kartoitus määritetään Commerce site builderin **Sivuston asetukset** -kohdassa **Kanavat**-sivulla. 

Jos pyynnön URL-osoite ei vastaa mitään URL-osoitetta, joka on yhdistetty asiakkaan maahan, vastauksessa palautetaan luettelo yhdestä tai useammasta kyseiseen maahan yhdistetystä URL-osoitteesta. Maan tai alueen valitsin vertaa luettelossa jokaista URL-osoitetta URL-osoitteisiin, jotka on konfiguroitu maa- tai aluemoduulissa. Aina kun haku löytyy, maan tai alueen valitsin muodostaa URL-osoitteen näyttöotsikon, alaotsikon ja kuvan sekä hyperlinkit URL-osoitteen avulla.

Kun asiakas valitsee maan tai alueen valitsimessa, hän käyttää hyperlinkki-URL-osoitetta. URL-osoite kirjoitetaan **\_msdyn365\_\_\_site\_**-evästeeseen, jotta sitä voi käyttää asiakkaan sivustoviittauksena. Kun asiakas pyytää seuraavan kerran URL-osoitetta, joka ei liity asiakkaan maahan tai alueeseen, järjestelmä ohjaa ne automaattisesti ensisijaiseen maahansa. Siksi on suositeltavaa käyttää myös sähköisen kauppasivuston [sivuston valitsinmoduulia](site-selector.md), jotta asiakkaat voivat ohittaa tai päivittää sivustoasetuksensa. 

Jos asiakas sulkee maan tai alueenvalitsimen valintaikkunan, keksiä ei kirjoitetaan ja asiakas pysyy nykyisessä sivustossa. 

Seuraavassa kuvassa on esimerkki maan tai alueen valitsimen valintaikkunasta.

![Esimerkki maan tai alueen valitsimen valintaikkunasta aloitussivulla.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Maan tai alueen valitsinmoduulin ominaisuudet

| Ominaisuuden nimi              | Arvo       | kuvaus                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Otsikko                    | Teksti        | Valintaikkunan yläosassa näkyvä otsikko.       |
| Alaotsikko                 | Teksti        | Otsikon alapuolella oleva alaotsikko.               |
| Maa: Näytön merkkijono    | Teksti        | URL-vaihtoehdon näyttönimi (esim. Kanada).   |
| Maa: Näytön alimerkkijono | Teksti        | URL-vaihtoehdon valinnainen näytön alimerkkijono (esim. "englanti" tai "ranska"). |
| Maa: Maakuva     | Mediaresurssi | URL-vaihtoehtoon yhdistetty valinnainen kuva (esim. Kanadan lipun kuva). |
| Maa: Maan URL       | Teksti        | Määritettävän maan/alueen sivuston URL-osoite. Tämän URL-osoitteen on vastattava täsmälleen URL-osoitetta, jonka määritit tälle maalle/alueelle Commerce-sivuston rakennustyökalun **Kanavat**-sivulla **Sivuston asetukset** -kohdassa. Lisäksi URL-osoitteen toimialueen on oltava **Kanavien**-sivun **Täsmäytä toimialue** -kentässä määritetty mukautettu toimialue, ei Commercen sivuston (esimerkiksi URL-osoite `https://<yourcompany>.commerce.dynamics.com/`) käyttöosoitetta. |
| Toimintolinkki                | Toimintolinkki | Valinnainen linkki, joka näkyy valintaikkunan alaosassa. Tämä linkki voi viedä esimerkiksi sisäiselle sivulle, joka sisältää luettelon kaikista sivuston tukemista maista ja alueista. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Maan tai alueen valitsinmoduulin lisääminen sivulle

Maan tai alueen valitsinmoduulin voi lisätä otsikkomoduuliin joko suoraan tai yhteisen katkelman avulla. Lisätietoja otsikkomoduuleista: [Otsikkomoduuli](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Maan tai alueen valitsinmoduulin määrittäminen Commercen sivustonluontiohjelmassa

> [!NOTE]
> Asiakkaille suosittelemiasi URL-osoitteet on määritettävä maaobjekteiksi maan tai alueen valitsinmoduulissa.

Noudata Commercen sivustonluontiohjelmassa seuraavia ohjeita kaikkien niiden sivusto-URL-osoitteiden osalta, jotka haluat näyttää ja antaa suosituksena asiakkaille.

1. Valitse maan tai alueen valitsinmoduulin paikka.
1. Valitse ominaisuusruudun **Maaluettelo**-kohdassa **Lisää maa**.
1. Valitse uusi **Maa**-ikkuna.
1. Anna **Näytön merkkijono** -kentässä näyttönimi (esimerkiksi **Kanada**).
1. Valinnainen: anna **Näytön alimerkkijono** -kentässä näytön alimerkkijono (kuten **ranska** tai **fr-ca**).
1. Valinnainen: Valitse kuva mediakirjastosta.
1. Kirjoita **Maan URL**-kenttään URL-osoite. Tämän URL-osoitteen on oltava täsmälleen sama kuin **Kanavat**-sivulla näkyvän URL-osoitteen ja joka yhdistetään kanavaan sisältäen sijainnin, joka on yhdistetty maahan tai alueeseen. 
1. Valitse **OK**.
1. Toista nämä vaiheet kaikkien muiden URL-osoitteiden osalta, joiden haluat näkyvän maan tai alueen valitsinmoduulissa.

## <a name="additional-resources"></a>Lisäresurssit

[Maantieteellisen sijainnin tunnistuksen ja uudelleenohjauksen määritys](geo-detection-redirection.md)

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ylätunnistemoduuli](author-header-module.md)

[Sivuston valitsinmoduuli](site-selector.md)

[Navigointipolkumoduuli](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
