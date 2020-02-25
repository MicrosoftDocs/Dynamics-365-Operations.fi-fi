---
title: Myyntipisteen asettelun suunnittelutoiminnon asentaminen
description: Voit käyttää yhden napsautuksen suunnittelutoimintoa Modern POS:n (MPOS) ja Cloud POS:n asettelusta, vaakasuunnassa tai pystytilassa, kaupat, kassakoneet, kassat ja esimiehet suunnittelussa.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9882ae895de926e0da3579ab65a988f2b97f7be
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022457"
---
# <a name="install-the-pos-layout-designer"></a>Myyntipisteen asettelun suunnittelutoiminnon asentaminen

[!include [banner](includes/banner.md)]

Voit käyttää yhden napsautuksen suunnittelutoimintoa Modern POS:n (MPOS) ja Cloud POS:n asettelusta, vaakasuunnassa tai pystytilassa, kaupat, kassakoneet, kassat ja esimiehet suunnittelussa.

MPOS tai Cloud POS  -käyttöliittymän graafinen rakenne määräytyy kassan asettelun mukaan. Rakenne määrää eri objektien sijainnin. Esimerkiksi kokonaisarvon asettelun, nimikeruudukon asettelun, asiakkaan asettelun, maksun asettelua ja eri valikkopainikkeiden asettelua. Asettelut sisältävät myös myynnin liittymän ulkoasun, joka näkyy työntekijöille .

## <a name="install-the-one-click-designer"></a>Asenna yhden napsautuksen suunnittelutoiminto

1. Valitse Kaupan vasemmassa yläkulmassa olevasta valikosta **Vähittäismyynti ja kauppa** &gt; **Kanavan asetukset** &gt; **POS-asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.
2. Valitse asettelu, jonka sovellustyyppi on **Modern POS Windowsille** tai **Vähittäismyynnin pilvimyyntipiste**, ja valitse sitten **asettelun suunnittelutoiminto**.
3. Napsauta Internet Explorer -ikkunan alaosassa näkyvällä ilmoitusrivillä **Avaa** aloittaaksesi yhden napsautuksen suunnittelutoiminnon asennuksen. (Ilmoitusrivi saattaa näkyä eri kohdassa muissa selaimissa.)
4. **Sovellus suoritetaan - suojauksen varoitus** viesti tulee näkyviin, valitse **suorita** joka asentaa vähittäismyynnin suunnittelutyökalun isännän. Edistymisen ilmaisin näyttää asennusprosessin edistymisen tilanteen.
5. Kun asennus on päättynyt, anna kaupan käyttäjänimesi ja salasanasi **Kirjaudu sisään** -sivulla ja aloita sitten suunnittelutoiminto valitsemalla **Kirjaudu sisään**.
6. Kun tunnistetietosi on tarkistettu ja suunnittelutoiminta alkaa, voit aloittaa oman asettelun suunnittelun tai aiemmin luodun asettelun muokkaamisen.

    [![Asettelu yhdenklikkauksen suunnitteluohjelmassa](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Asettelun suunnittelutoiminto asennuksen vianmääritys

- Kun valitset **Suunnittelutoiminto**, lataa (tai suorita) asennusohjelma kehote ei näy tai nykyiset suojausasetukset ei salli Lataa tiedosto. 

    **Ratkaisut:**

    - Tarkista Internet Explorerissa, että ponnahdussanoman esto on poistettu käytöstä tälle sivustolle. Valitse **Asetukset** &gt; **Vaihtoehdot** &gt; **Tietosuoja** &gt; **Etsi ponnahdussanoman esto** ja muuta asetusta, jos se on pakollinen.
    - Lisää Internet Explorerissa Kaupan URL-osoite luotettuihin sivustoihin. Valitse **Asetukset** &gt; **vaihtoehdot** &gt; **suojaus** &gt; **Luotettavat sivustot** &gt; **sivustot** &gt; **Lisää**.

- Ohjelma ei käynnisty ja ohjeiden mukaisesti voit ottaa yhteyttä toimittajaan.

    **Ratkaisu:** Lisää Internet Explorerissa Kaupan URL-osoite luotettuihin sivustoihin. Valitse **asetukset** &gt; **vaihtoehdot** &gt; **suojaus** &gt; **Luotetut sivustot** &gt; **sivustot** &gt; **Lisää**.

**Tunnettu ongelma:** suunnittelu ei toimi oikein Google Chrome- eikä Firefox-selaimessa. Ratkaisemme parhaillaan tätä ongelma.

## <a name="additional-resources"></a>Lisäresurssit

[Retail Modern POS:n (MPOS) määrittäminen, asentaminen ja aktivoiminen](retail-modern-pos-device-activation.md)
