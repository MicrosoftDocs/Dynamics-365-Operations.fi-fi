---
title: Kiinteä vastaanottohinta
description: Tässä artikkelissa on tietoja kiinteiden vastaanottohintojen konfiguroinnista ja käytöstä Microsoft Dynamics 365 Supply Chain Managementissa.
author: raprofit
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 2630952f395d1a18202698b4d73b67ef4b760194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907577"
---
# <a name="fixed-receipt-price"></a>Kiinteä vastaanottohinta

[!include [banner](../includes/banner.md)]

**Kiinteä vastaanottohinta** on vaihtoehto, jonka voit valita nimikemalliryhmälle käytettäessä muuta varastomallia kuin *Vakiokustannus* tai *Liukuva painotettu keskiarvo* . Tämän vaihtoehdon nimi oli Microsoft Dynamics AX:n varhaisissa versioissa **Vakiokustannus**. Nimi muutettiin **kiinteäksi vastaanottohinnaksi** uudessa standardikustannusvarastomallissa Dynamics AX 2012 -versiossa. Tässä artikkelissa on tietoja kiinteiden vastaanottohintojen konfiguroinnista ja käytöstä Dynamics 365 Supply Chain Managementissa.

## <a name="about-fixed-receipt-prices"></a>Tietoja kiinteästä vastaanottohinnasta

Kun valitset nimikkeelle **Kiinteän vastaanottohinta** -valintaruudun **Nimikemalliryhmä**-sivulla, järjestelmä käyttää vastaanottohintaa varaston vastaanoton standardikustannuksena. Jos tuotteelle määritetty ostohinta ja nimikkeen oletuskustannushinta eroavat toisistaan, ero kirjataan **Kiinteän vastaanottohinnan voitto**- tai **Kiinteä vastaanottohinnan tappio** -tilille ja vastakirjaus **Varaston kirjausprofiili** -sivulla määritetylle **kiinteän vastaanottohinnan vastatilille**.

Koska **Kiinteä vastaanottohinta** -vaihtoehtoa käytetään yhdessä eri varastomallien kanssa (esimerkiksi FIFO (first in, first out), LIFO (last in, first out) ja painotettu keskiarvo), *varaston sulkemis- ja oikaisuprosessi* luo edelleen täsmäytykset ja oikaisut **Nimikemalliryhmä**-sivulla valittavan varastoperiaatteen mukaisesti. Oikaisut tehdään kuitenkin vain varasto-ottoihin varastosta.

Olet konfiguroinut tuotteen esimerkiksi nimikemalliryhmällä, jossa **Varastomalli**-kentän arvona on *FIFO*, ja **Kiinteä vastaanottohinta** -vaihtoehto on valittu. Kun varastoa vastaanotetaan ostotilauksen kautta, varaston arvoksi määritetään nimikkeen oletuskustannushinta tuotteen vastaanottohetkellä. Kun laskutat ostotilauksen, jos laskun hinta on eri, järjestelmä kirjaa vapautetun tuotteen oletuskustannushinnan varastotilille. Se kirjaa eron kiinteän vastaanottohinnan tuotto- tai tappiotilille. Myöhemmin, kun tuote myydään tai kulutetaan, järjestelmä käyttää nimikkeen liukuvaa keskiarvoa myyntitilauslaskun kirjaamisen yhteydessä (paitsi jos käytät merkintää).

Kun suoritat *varaston sulkemis- ja oikaisuprosessin*, järjestelmä luo täsmäytyksen, jossa ensimmäinen varasto-otto täsmäytetään ensimmäistä vastaanottoa vasten. Vastaanotossa käytetyn vastaanottohinnan ja varasto-otossa käytetyn liukuvan keskiarvon välinen ero kirjataan uuteen tositteeseen.

## <a name="enable-fixed-receipt-prices"></a>Ota kiinteät vastaanottohinnat käyttöön

Ota nimikkeelle kiinteät vastaanottohinnat käyttöön noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Nimikemalliryhmät**.
2. Luo uusi nimikemalliryhmä tai valitse aiemmin luotu nimikemalliryhmä.
3. Valitse **Kustannuslaskentamenetelmä ja kustannuksen tunnistaminen** -pikavälilehdessä **Kiinteä vastaanottohinta** -valintaruutu.

    > [!NOTE]
    > **Kiinteä vastaanottohinta** -valintaruutua ei voi valita, jos **Varastomalli**-kentänarvoksi on määritetty *Vakiokustannus* tai *Liukuva keskiarvo*.

4. Sulje sivu.

Kun olet ottanut **kiinteän vastaanottohinnan** käyttöön, varaston kirjausprofiili on päivitettävä seuraavien vaiheiden mukaisesti.

1. Siirry kohtaan **Varastonhallinta \> Määritys \> Kirjaus \> Kirjaus**.
1. Valitse **Ostotilaus**-välilehden **Valitse**-sarakkeesta **Kiinteän vastaanottohinnan tuotto**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Määritä uusi rivi niin, että sitä käytetään nimikemalliryhmässä, jossa olet ottanut kiinteän vastaanoton hinnoittelun käyttöön, ja määritä päätili, jota käytetään ostotilausten kiinteän vastaanottohinnan voittojen kirjaamiseen. Määritä muut asetukset tarpeen mukaan.
1. Valitse **Valitse**-sarakkeesta **Kiinteä vastaanottohinnan tappio**. Lisää uusi rivi niin, että sitä käytetään nimikemalliryhmässä, jossa olet ottanut kiinteän vastaanoton hinnoittelun käyttöön, ja määritä päätili, jota käytetään ostotilausten kiinteän vastaanottohinnan tappioiden kirjaamiseen. Määritä muut asetukset tarpeen mukaan.
1. Valitse **Valitse**-sarakkeesta **Kiinteä vastaanottohinnan vastatili**. Lisää uusi rivi niin, että sitä käytetään nimikemalliryhmässä, jossa olet ottanut kiinteän vastaanoton hinnoittelun käyttöön, ja määritä päätili, jota käytetään ostotilausten kiinteän vastaanottohinnan vastakirjausten kirjaamiseen. Määritä muut asetukset tarpeen mukaan.
1. Valitse **Varasto**-välilehden **Valitse**-sarakkeesta **Kiinteän vastaanottohinnan tuotto**. Lisää uusi rivi niin, että sitä käytetään nimikemalliryhmässä, jossa olet ottanut kiinteän vastaanoton hinnoittelun käyttöön, ja määritä päätili, jota käytetään varaston kiinteän vastaanottohinnan voittojen kirjaamiseen. Määritä muut asetukset tarpeen mukaan.
1. Valitse **Valitse**-sarakkeesta **Kiinteä vastaanottohinnan tappio**. Lisää uusi rivi niin, että sitä käytetään nimikemalliryhmässä, jossa olet ottanut kiinteän vastaanoton hinnoittelun käyttöön, ja määritä päätili, jota käytetään varaston kiinteän vastaanottohinnan tappioiden kirjaamiseen. Määritä muut asetukset tarpeen mukaan.

> [!NOTE]
> On suositeltavaa, että **Kiinteän vastaanottohinnan voitto**- ja **Kiinteän vastaanottohinnan tappio** -kentissä käytetään samaa päätiliä sekä ostotilauksille että varastolle.

> [!IMPORTANT]
> Kun muutat **Vapautetut tuotteet** -sivun **Kustannusten hallinta** -pikavälilehden **Hinta**-kentän arvoa, järjestelmä ei uudelleenarvosta automaattisesti käytettävissä olevaa varastoa. Voit suorittaa manuaalisen kiertotavan avaamalla **Sulkeminen ja oikaisu** -sivun ja valitsemalla toimintoruudusta **Oikaisu \> Varastosaldo**. Valitse sitten nimikkeet, joita on saatavilla, ja oikaise ne nykyiseen hintaan. Vakiokustannusvarastomallin käyttämisestä on yksi selvä etu siinä, että järjestelmä uudelleenarvostaa käytettävissä olevan varaston automaattisesti.
