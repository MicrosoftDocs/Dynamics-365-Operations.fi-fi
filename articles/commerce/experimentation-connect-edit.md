---
title: Kokeen yhdistäminen ja variaatioiden muokkaaminen
description: Tässä artikkelissa käsitellään kolmannen osapuolen palvelussa olevan kokeen yhdistämistä Dynamics 365 Commerceen ja kokeen variaatioiden muokkaamista.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942819"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Kokeen yhdistäminen ja variaatioiden muokkaaminen

Tässä artikkelissa käsitellään kokeen yhdistämistä Commercessa ja muutosten tekemistä variaatioihin siten, että ne vastaavat hypoteesia. 

Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä artikkeleissa.

[ ![Kokeilun käyttäjän siirtymä – yhdistäminen ja muokkaaminen.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Sen jälkeen kun [koe on määritetty](experimentation-setup.md) kolmannen osapuolen palvelussa, koe yhdistetään Dynamics 365 Commercessa, jossa muokataan kokeen variaatioita.

## <a name="connect-your-experiment"></a>Kokeen yhdistäminen
Yhdistä koe käynnistämällä ohjattu **Yhdistä koe** -toiminto. Ohjattu toiminto opastaa kokeen yhdistämisvaiheissa. Kun ohjattu toiminto on suoritettu, koe on yhdistetty sekä variaatiot luotu ja valmiita muokattaviksi.

Kokeen yhdistäminen Commercen sivustonmuodostimeen aloitetaan seuraavasti:

1. Käynnistä ohjattu **Yhdistä koe** -toiminto valitsemalla vasemmassa siirtymisruudussa **Kokeet** ja valitsemalla sitten **Yhdistä**. Vaihtoehtoisesti voit käyttää ohjattua toimintoa sivu- tai osaeditorista muokkaamalla sitä tai valitsemalla komentopalkissa **Yhdistä koe**.

    > [!NOTE]
    > - Sivu voidaan yhdistää kerrallaan vain yhteen kokeeseen. Voit yhdistää sivun toiseen kokeeseen poistamalla ensin kokeen sivulta, johon se on nyt yhdistetty.
    > - Voit kokeilla vain mukautettua asettelua käyttävillä sivuilla. Jos sivulla on esimääritetty asettelu, muunna se ensin mukautetuksi asetteluksi. Voit tehdä tämän menemällä sivulle ja valitsemalla komentopalkissa **Muunna mukautetuksi asetteluksi**. Lisätietoja asetteluista on kohdassa [Esimääritetyt ja mukautetut asettelut](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Jos muodostat yhteyden kokeiluun vasemman siirtymisruudun **Kokeilut**-välilehdessä, valitse haluamasi kokeilun nimi näkyviin tulevasta luettelosta.
1. Valitse sivu tai osa, jossa haluat suorittaa kokeilun.
1. Valitse ohjatun toiminnon viimeisessä vaiheessa **Luo variaatiot ja lopeta ohjattu toiminto**. Variaatiot luodaan kokeelle. 

> [!NOTE]
> Jos haluat aikatauluttaa kokeen julkaisun live-sivustoon, varmista, että kokeeseen liitettävä sisältö on saatavana julkaisuryhmässä *ennen* kokeen yhdistämistä. Lisätietoja julkaisuryhmistä on kohdassa [Julkaisuryhmien kanssa työskenteleminen](publish-groups.md).

## <a name="edit-your-variations"></a>Variaatioiden muokkaaminen

Variaatiot luodaan, kun lopetat **Yhdistä kokeilu** -ohjatun toiminnon. Noudata alla olevia vaiheita muokataksesi variaatiot vastaamaan valintoja, jotka on vahvistettava kokeen hypoteesi.

1. Muokkaa editorinäkymässä komentopalkin alapuolella olevan variaatioiden avattavan valikon avulla kutakin variaatiota alkuperäisen hypoteesin perusteella. Yhtä variaatioista kannattaa ehkä olla muuttamatta, jolloin se toimii vertailu- tai perusvariaationa.
1. Valitse moduuli, jossa koe tehdään, valitsemalla kolme pistettä (....). Valitse lopuksi **Lisää kokeeseen**.

> [!NOTE]
> Yhtä variaatioista kannattaa ehkä olla muuttamatta, jolloin se toimii vertailu- tai perusvariaationa.

## <a name="previous-step"></a>Edellinen vaihe
[Kokeen määrittäminen](experimentation-setup.md) 


## <a name="next-step"></a>Seuraava vaihe
[Kokeen esikatseleminen ja julkaiseminen](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
