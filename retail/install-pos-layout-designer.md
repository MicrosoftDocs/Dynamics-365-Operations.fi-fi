---
title: Retail POS-asettelun suunnittelutoiminto asentaminen
description: "Voit käyttää yhden napsautuksen suunnittelutoimintoa Cloud POS:n ja Retail Modern POS:n (MPOS) asettelusta, vaakasuunnassa tai pystytilassa, kaupat, kassakoneet, kassat ja esimiehet suunnittelussa."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e60994f5c4fa38fc2be17b4021e2def904c87b7f
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="install-the-retail-pos-layout-designer"></a>Retail POS-asettelun suunnittelutoiminto asentaminen

[!include[banner](includes/banner.md)]


Voit käyttää yhden napsautuksen suunnittelutoimintoa Cloud POS:n ja Retail Modern POS:n (MPOS) asettelusta, vaakasuunnassa tai pystytilassa, kaupat, kassakoneet, kassat ja esimiehet suunnittelussa.

MPOS tai Cloud POS  -käyttöliittymän graafinen rakenne määräytyy kassan asettelun mukaan. Rakenne määrää eri objektien sijainnin. Esimerkiksi kokonaisarvon asettelun, nimikeruudukon asettelun, asiakkaan asettelun, maksun asettelua ja eri valikkopainikkeiden asettelua. Asettelut sisältävät myös myynnin liittymän ulkoasun, joka näkyy työntekijöille .

## <a name="install-the-one-click-designer"></a>Asenna yhden napsautuksen suunnittelutoiminto
1.  Microsoft Dynamics 365 for Operations -järjestelmän vasemman yläkulman valikon avulla voit siirtyä **Vähittäismyynti** **ja kauppa** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipiste** &gt; **Näytön asettelut**.
2.  Valitse asettelu, jonka sovellustyyppi on **Modern POS Windowsille** tai **Vähittäismyynnin pilvimyyntipiste**, ja valitse sitten **asettelun suunnittelutoiminto**.
3.  Napsauta Internet Explorer -ikkunan alaosassa näkyvällä ilmoitusrivillä **Avaa** aloittaaksesi yhden napsautuksen suunnittelutoiminnon asennuksen. (Ilmoitusrivi saattaa näkyä eri kohdassa muissa selaimissa.)
4.  **Sovellus suoritetaan - suojauksen varoitus** viesti tulee näkyviin, valitse **suorita** joka asentaa vähittäismyynnin suunnittelutyökalun isännän. Edistymisen ilmaisin näyttää asennusprosessin edistymisen tilanteen.
5.  Kun asennus on päättynyt, syötä Microsoft Dynamics 365 for Operations -käyttäjänimesi ja salasanasi **Kirjaudu sisään** -sivulla ja valitse sitten **Kirjaudu sisään** aloittaaksesi suunnittelutoiminnon.
6.  Kun tunnistetietosi on tarkistettu ja suunnittelutoiminta alkaa, voit aloittaa oman asettelun suunnittelun tai aiemmin luodun asettelun muokkaamisen. [![Asettelu yhdenklikkauksen suunnitteluohjelmassa](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Asettelun suunnittelutoiminto asennuksen vianmääritys
-   Kun valitset **Suunnittelutoiminto**, lataa (tai suorita) asennusohjelma kehote ei näy tai nykyiset suojausasetukset ei salli Lataa tiedosto. **Ratkaisut:**
    -    Internet Explorerissa tarkista, että ponnahdussanoman esto on poistettu käytöstä tälle sivustolle. Valitse **Asetukset** &gt; **Vaihtoehdot** &gt; **Tietosuoja** &gt; **Etsi ponnahdussanoman esto** ja muuta asetusta, jos se on pakollinen.
    -   Lisää Internet Explorerissa Dynamics 365 for Operations -osoite luotettuihin sivustoihin. Valitse **Asetukset** &gt; **vaihtoehdot** &gt; **suojaus** &gt; **Luotettavat sivustot** &gt; **sivustot** &gt; **Lisää**.
-   Ohjelma ei käynnisty ja ohjeiden mukaisesti voit ottaa yhteyttä toimittajaan. **Ratkaisu:** Lisää Internet Explorerissa Dynamics 365 for Operations -osoite luotettuihin sivustoihin. Valitse **asetukset** &gt; **vaihtoehdot** &gt; **suojaus** &gt; **Luotetut sivustot** &gt; **sivustot** &gt; **Lisää**.

**Tunnettu ongelma:** suunnittelu ei toimi oikein Google Chrome- eikä Firefox-selaimessa. Ratkaisemme parhaillaan tätä ongelma.

<a name="see-also"></a>Lisätietoja
--------

[Määritä, Lataa, asentaa ja ottaa käyttöön Retail Modern POS](retail-modern-pos-device-activation.md)




