---
title: Kokeen yhdistäminen ja variaatioiden muokkaaminen
description: Tässä ohjeaiheessa käsitellään kolmannen osapuolen palvelussa olevan kokeen yhdistämistä Dynamics 365 Commerceen ja kokeen variaatioiden muokkaamista.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930190"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Kokeen yhdistäminen ja variaatioiden muokkaaminen

Tässä ohjeaiheessa käsitellään kokeen yhdistämistä Commercessa ja muutosten tekemistä variaatioihin siten, että ne vastaavat hypoteesia. Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä ohjeaiheissa.

[ ![Kokeilun käyttäjän siirtymä – yhdistäminen ja muokkaaminen](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Sen jälkeen kun [koe on määritetty](experimentation-setup.md) kolmannen osapuolen palvelussa, koe yhdistetään Dynamics 365 Commercessa, jossa muokataan kokeen variaatioita.

## <a name="planning-considerations"></a>Suunnittelussa huomioon otettavaa

Ennen kuin koe yhdistetään Commercessa, sinun tehtävä päätöksiä, jotka vaikuttavat Commercen tapaan hallita sisältöä.

### <a name="determine-the-scope-of-your-experiment"></a>Kokeen laajuuden määrittäminen
Koetta yhdistettäessä sinua pyydetään määrittämään kokeen laajuus. Kokeen laajuudeksi määritetään **osittainen**tai **kokonaan**.
- Valitse **osittainen**, jos haluat suorittaa kokeen tietyssä sivun osassa. Jos valitset tämän vaihtoehdon, sinun on määritettävä, mikä moduuleista sisältyy kokeeseen. Oletussivun osiin tai osiin, jotka eivät liity kokeen, tehdyt muutokset synkronoidaan automaattisesti variaatioiden välillä.
- Valitse **kokonaan**, jos haluat suorittaa kokeen koko sivulla tai osassa. Oletussivusta tai osasta luodaan erilliset kopiot. Kokeeseen sisältyviä moduuleja ei tarvitse valita, sillä koko muokkausalaa voidaan muuttaa. Voit tarpeen mukaan lisätä, poistaa ja järjestää moduuleja uudelleen. Jos muutokset kuitenkin tehdään oletussivulle tai osalle, johon koe on liitetty, kyseiset muutokset on synkronoitava manuaalisesti eri variaatioihin.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Jos liität kokeen asettelua käyttävään sivuun, kokeen mahdollinen laajuus on **kokonaan**.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Kokeen julkaisun mahdollisesta aikatauluttamisesta päättäminen
Jos haluat aikatauluttaa kokeen julkaisun live-sivustoon, varmista, että kokeeseen liitettävä sisältö on saatavana julkaisuryhmässä *ennen* kokeen yhdistämistä. 

Lisätietoja julkaisuryhmistä on kohdassa [Julkaisuryhmien kanssa työskenteleminen](publish-groups.md).


## <a name="connect-your-experiment"></a>Kokeen yhdistäminen
Yhdistä koe käynnistämällä ohjattu **Yhdistä koe** -toiminto. Ohjattu toiminto opastaa kokeen yhdistämisvaiheissa. Kun ohjattu toiminto on suoritettu, koe on yhdistetty sekä variaatiot luotu ja valmiita muokattaviksi.

1. Käynnistä ohjattu toiminto valitsemalla **Kokeet**-välilehti sivustonmuodostimessa ja valitse sitten **Yhdistä**. Ohjattua toimintoa voidaan käyttää myös sivu- tai osaeditorista. Valitse muokkaustilan komentopalkissa **Yhdistä koe**.

> [!NOTE]
> Sivu voidaan yhdistää kerrallaan vain yhteen kokeeseen. Voit yhdistää sivun toiseen kokeeseen poistamalla ensin kokeen sivulta, johon se on nyt yhdistetty.

1. Valitse sivu tai osa, jossa haluat suorittaa kokeilun.
1. Määritä kokeilun laajuudeksi **osittainen** tai **kokonaan** sen mukaan, mitä valittiin edellä olevassa kohdassa [Kokeen laajuuden määrittäminen](#determine-the-scope-of-your-experiment).
    > [!NOTE]
    > **Koe sivuilla tai osissa** -ominaisuusmerkintä on oltava käytössä jos haluat tehdä kokeen koko sivulla tai koko osassa. Lisätietoja on kohdassa [Kokeilu Dynamics 365 Commercessa](experimentation-overview.md).
    
1. Valitse ohjatun toiminnon viimeisessä vaiheessa **Luo variaatiot ja lopeta ohjattu toiminto**. Variaatiot luodaan kokeelle. 

## <a name="edit-your-variations"></a>Variaatioiden muokkaaminen
Variaatiot luodaan, kun lopetat ohjatun toiminnon. 

Seuraavaksi muokataan variaatiot vastaamaan valintoja, jotka on vahvistettava kokeen hypoteesi. Valitse jokin seuraavista menetelmistä, joka vastaa edellä käsitellyssä kohdassa [Kokeen laajuuden määrittäminen](#determine-the-scope-of-your-experiment) kokeeseen valittua laajuutta.

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Osittaisen laajuuden kokeiden variaatioiden muokkaaminen
Toimi seuraavasti, jos määritit kokeen laajuudeksi **osittainen** ohjatussa **Yhdistä koe** -toiminnossa.

1. Muokkaa editorinäkymässä komentopalkin alapuolella olevan variaatioiden avattavan valikon avulla kutakin variaatiota alkuperäisen hypoteesin perusteella. Yhtä variaatioista kannattaa ehkä olla muuttamatta, jolloin se toimii vertailu- tai perusvariaationa.
1. Valitse moduuli, jossa koe tehdään, valitsemalla kolme pistettä (....). Valitse lopuksi **Lisää kokeeseen**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Koko laajuuden kokeiden variaatioiden muokkaaminen
Jos kokeen laajuudeksi määritettiin **kokonaan** ohjatussa **Yhdistä koe** -toiminnossa, editorinäkymän komentopalkin alapuolella olevan variaatioiden avattavan valikon avulla voi muokata kutakin variaatiota alkuperäisen hypoteesin perusteella. 

> [!NOTE]
> Kummassakin tapauksessa yksi variaatioista kannattaa ehkä jättää muuttamatta, jolloin se toimii vertailu- tai perusvariaationa.

## <a name="previous-step"></a>Edellinen vaihe
[Kokeen määrittäminen](experimentation-setup.md) 


## <a name="next-step"></a>Seuraava vaihe
[Kokeen esikatseleminen ja julkaiseminen](experimentation-preview-publish.md)
