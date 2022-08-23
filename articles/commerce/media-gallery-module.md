---
title: Mediavalikoimamoduuli
description: Tässä artikkelissa on tietoja mediavalikoimamoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5e2d0a4422341badee906c71bebdd491e18a38cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273455"
---
# <a name="media-gallery-module"></a>Mediavalikoimamoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja mediavalikoimamoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Mediavalikoimamoduuleissa on yksi kuva tai useita kuvia valikoimanäkymässä. Mediavalikoimamoduulit tukevat pikkukuvia. Ne voivat olla vaakasuuntaisesti (rivinä kuvan alla) tai pystysuuntaisesti (pystyrivinä kuvan vieressä). Mediavalikoimamoduulit sisältävät myös ominaisuuksia, joiden avulla kuvia voi zoomata (suurentaa) tai tarkastella koko näytön tilassa. Kuvan on oltava käytettävissä Commercen sivustonmuodostimen mediakirjastossa, jotta se voidaan hahmontaa mediavalikoimamoduuliin. Tällä hetkellä mediavalikoimamoduulit tukevat vain kuvia.

Oletustilassa mediavalikoimamoduuli käyttää tuotetunnusta, joka on käytettävissä tuotetietojen sivun (PDP) sivukontekstissa. Sen avulla hahmonnetaan vastaavat tuotekuvat. Commercen pääkonttoriversiossa mediatiedostopolku on määritettävä kaikille tuotteille. Tämän jälkeen kuvat on ladattava sivustonmuodostimen mediakirjastoon sen tiedostopolun mukaan, joka on määritetty tuotteille Commercen pääkonttorisovelluksessa. Nämä kuvat sisältävät kuvia tuotteista ja mahdollisista tuoteversioista. Lisätietoja kuvien lataamisesta sivustonmuodostimen mediakirjastoon on kohdassa [Kuvien lataaminen](dam-upload-images.md).

Vaihtoehtoisesti mediavalikoimamoduuli voi isännöidä täysin kuratoitua tuotejoukkoa kuvavalikoimasivulla, jossa ei ole tuotetunnuksen tai sivun kontekstin riippuvuuksia. Tässä tapauksessa kuvat on ladattava sivustonmuodostimen mediakirjastoon ja määritettävä sivustonmuodostimessa.

Tässä on joitakin mediavalikoimamoduulien käyttöesimerkkejä:

- Tuotekuvien hahmontaminen PDP:ssä
- Tuotekuvien hahmontaminen tuotteen markkinointisivulla
- Kuratoidun kuvajoukon esitteleminen markkinointisivulla, kuten valikoimasivulla

Seuraavassa esimerkissä PDP:n ostoruutu isännöi tuotekuvia mediavalikoimamoduulin avulla.

![Esimerkki ostoruudusta tuotetietosivulla, joka isännöi tuotekuvia mediavalikoimamoduulin avulla.](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Mediavalikoiman ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Kuvan lähde | **Sivun konteksti** tai **Tuotetunnus** | Oletusarvo on **Sivun konteksti**. Jos **Sivun konteksti** on valittuna, moduuli olettaa, että sivu antaa tuotetunnuksen tiedot. Jos **Tuotetunnus** on valittuna, kuvan tuotetunnus on annettava **Tuotetunnus**-ominaisuuden arvona. Tämä ominaisuus on käytettävissä Commercen versiossa 10.0.12. |
| Tuotetunnus | Tuotetunnus | Tämä ominaisuus on käytettävissä vain, jos **Kuvan lähde** -ominaisuuden arvo on **Tuotetunnus**. |
| Kuvan zoomaus | **Sisäinen** tai **Säilö** | Tämän ominaisuuden avulla käyttäjä voi zoomata kuvia mediavalikoimamoduulissa. Kuvaa voi zoomata sisäisesti tai erillisessä säilössä kuvan vieressä. Tämä ominaisuus on käytettävissä versiossa 10.0.12. |
| Zoomauskerroin | Desimaalinumero | Tämä ominaisuus määrittää kuvien zoomauksen skaalauskertoimen. Jos arvoksi on määritetty esimerkiksi **2,5**, kuvat suurennetaan 2,5 kertaisiksi. |
| Koko näyttö | **Tosi** vai **Epätosi** | Tämä ominaisuus määrittää, voidaanko kuvia tarkastella koko näytön tilassa. Koko näytön tilassa kuvia voidaan myös suurentaa entisestään, jos zoomausominaisuus on käytössä. Tämä ominaisuus on käytettävissä Commerce-version 10.0.13 julkaisussa. |
| Zoomatun kuvan laatu | Luku väliltä 1–100, joka edustaa prosenttilukua ja joka valitaan käyttämällä ohjauspalkkia. | Tässä ominaisuudessa määritetään kuvalaatu zoomatuille kuville. Sen arvoksi voidaan määrittää 100 prosenttia. Näin voidaan varmistaa, että zoomattu kuva käyttää aina suurinta mahdollista tarkkuutta. Tämä ominaisuus ei koske PNG-tiedostoja, koska ne käyttävät häviötöntä muotoa. Tämä ominaisuus on käytettävissä Commerce-version 10.0.19 julkaisussa. |
| Kuvat | Kuvat, jotka on valittu sivustonmuodostimen mediakirjastosta | Kuvia voidaan hahmontaa tuotteesta. Niitä voidaan kuratoida myös mediavalikoimamoduulista. Nämä kuvat lisätään käytettävissä oleviin tuotekuviin. Tämä ominaisuus on käytettävissä Commercen versiossa 10.0.12. |
| Pikkukuvan suunta | **Pysty** tai **vaaka** | Tämä ominaisuus määrittää, näytetäänkö pikkukuvat pysty- vai vaakanauhassa. |
| Muuttujan päätuotekuvien piilottaminen | **Tosi** vai **Epätosi** | Jos ominaisuuden arvoksi määritetään **Tosi**, kun muuttuja valitaan, päätuotteen kuvat piilotetaan, ellei muuttujalla ole kuvia. Tämä ominaisuus ei vaikuta tuotteisiin, joissa ei ole muuttujia. |
| Median päivittäminen dimension valinnassa | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvoksi on määritetty **Tosi**, mediakirjaston kuvat päivitetään, kun jokin dimensio (kuten väri, tyyli tai koko) valitaan ja jos kuva on saatavana. Tämä ominaisuus yksinkertaistaa selauskokemusta, koska jokaista tuotevarianttidimensiota ei tarvitse valita vastaavaa päivitettävää kuvaa varten. Tämä ominaisuus on käytettävissä **Lisäasetukset**-välilehdessä. |

> [!IMPORTANT]
> **Päivitä media dimensiota valittaessa** -ominaisuus on saatavana Commercen versiossa 10.0.21. Se edellyttää Commercen moduulikirjastopaketin 9.31 asentamista.

Seuraavassa kuvassa on esimerkki mediavalikoimamoduulista, jossa koko näytön ja zoomauksen asetukset ovat käytettävissä.

![Esimerkki mediavalikoimamoduulista, jossa koko näytön ja zoomauksen asetukset ovat käytettävissä.](./media/ecommerce-media-zoom.png)

Seuraavassa kuvassa on esimerkki mediavalikoimamoduulista, jossa on kuratoituja kuvia (eli määritettyjä kuvia, jotka eivät riipu tuotetunnuksesta tai sivun kontekstista).

![Esimerkki mediavalikoimamoduulista, jossa on kuratoituja kuvia.](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Kun kuvalähde johdetaan sivun kontekstista, kuvien noutamiseen käytetään PDP:n tuotetunnusta. Mediavalikoimamoduuli hakee kuvan tiedostopolun tuotteille Commerce Scale Unitin ohjelmistorajapintojen (API) avulla. Kuvat noudetaan sitten mediakirjastastosta siten, että ne voidaan hahmontaa moduulissa.

## <a name="add-a-media-gallery-module-to-a-page"></a>Mediavalikoimamoduulin lisääminen sivulle

Voit lisätä mediavalikoimamoduulin markkinointisivulle seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Markkinointimalli** ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse oletussivun **pääpaikassa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -dialogiruudussa, kohdan **Sivun nimi** alla, **Mediavalikoimasivu** ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kohdassa luomasi **Markkinointimalli** ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos haluat muokata sivun tietoja, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**. 
1. Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Mediavalikoima**-moduuli ja valitse sitten **OK**.
1. Valitse mediavalikoimamoduulin ominaisuusruudun **Kuvalähde**-kohdassa **Tuotetunnus**. Anna sitten **Tuotetunnus**-kenttään tuotetunnus.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Nyt tuotteen kuvien tulisi näkyä valikoimanäkymässä.
1. Jos haluat käyttää vain kuratoituja kuvia, valitse ominaisuusruudun **Kuvalähde**-kohdassa **Tuotetunnus**. Valitse sitten **Kuvat**-kohdassa **Lisää kuva** niin monta kertaa kuin vaaditaan kuvien lisäämiseksi mediakirjastoon.
1. Määritä haluamasi lisäominaisuudet, kuten **Kuvan zoomaus**, **Zoomauskerroin** ja **Pikkukuvien suuntaus**.
1. Kun olet valmis, valitse **Tallenna**. Valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[Konttimoduuli](add-container-module.md)

[Kuvien lataaminen palveluun](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
