---
title: Pankkitilin täsmäyttäminen
description: Tässä ohjeaiheessa kerrotaan, miten pankkitili täsmäytetään.
author: panolte
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c77d08d5877ab27f9b6549a5b2a666150938fc08
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899322"
---
# <a name="reconcile-a-bank-account"></a>Pankkitilin täsmäyttäminen

[!include[banner](../includes/banner.md)]

Kun saat pankin tiliotteen, sinun tulee täsmäyttää yrityksen pankkitapahtumat tiliotteen tapahtumien kanssa säännöllisin väliajoin.

Et voi täsmäyttää pankkitilin tiliotetta, jos tiliotteen yhdenkään sekin tai talletuskuittimaksun tila on **Odottaa peruutusta**. Kun tarkistaja on kirjannut tai hylännyt sekin palautuksen tai talletuskuittimaksun peruutuksen, tila ei ole enää **Odottaa peruutusta** ja voit täsmäyttää pankkitilin.

1.  Valitse **Maksuliikenteen hallinta** \> **Pankkitilit** \> **Pankkitilit**. Valitse pankkitilitiliotteen kanssa täsmäytettävä pankkitili ja valitse **Täsmäytä** > **Tilin täsmäytys**.

2.  Syötä tiedot **Tiliotteen päivämäärä**- ja **Tiliote**-kenttiin. **Loppusaldo**-kenttään syötetään pankkitilin saldo sellaisena kuin se näkyy pankin tiliotteessa.

3.  Avaa **Tilin täsmäytys** -sivu valitsemalla **Tapahtumat**.

4.  Valitse kunkin tiliotteessa olevan tapahtuman **Selvitetyt**-valintaruutu jos summa Dynamics 365 Finance -järjestelmässä vastaa tiliotteen summaa. Voit myös syöttää tai muokata arvoa **Pankkitapahtuman laji** -kentässä. Tämän kentän arvo on tärkeä pankkitapahtumien tilastojen sekä muutamien raporttien kannalta.
    

    > [!NOTE]
    > <P>Älä valitse sellaisten tapahtumien <STRONG>Selvitetyt</STRONG>-valintaruutua, jotka eivät ole tiliotteessa. Nämä tapahtumat näkyvät edelleen tällä sivulla, kunnes ne myöhemmin täsmäytetään tiliotteen kanssa.</P>
    > <P><STRONG>Selvitetyt</STRONG>-valintaruutu ei ole käytettävissä, jos tapahtuman tila on <STRONG>Odottaa peruutusta</STRONG>. Tapahtumilla voi olla tämä tila, jos Finance on määritetty siten, että palautukset tai peruutukset on lähetettävä tarkistettaviksi ennen kirjaamista. Kun tarkistaja on kirjannut tai hylännyt sekin palautuksen tai talletuskuittimaksun peruutuksen, tila ei ole enää <STRONG>Odottaa peruutusta</STRONG> ja voit täsmäyttää pankkitilin tiliotteen kanssa.</P>

    
    Jos haluat valita **Selvitetyt**-valintaruudun sekkivälille, jotka kaikki näkyvät tiliotteessa, valitse **Merkitse sekkiväli** ja määritä sitten kyseinen väli.

5.  Jos pankkitilitapahtuman summa ei vastaa tiliotteen tapahtuman summaa, syötä korjauksen summa **Oikaisusumma**-kenttään.
    

    > [!NOTE]
    > <P>Jos korjattavan tapahtuman tilikausi on suljettu, <STRONG>Oikaisusumma</STRONG>-kenttää ei voi käyttää. Luo sen sijaan avoimeen tilikauteen korjausta varten uusi rivi, jolla on tapahtuman päivämäärä. Tässä tapauksessa sinun on lisättävä taloushallinnon dimensiot, joita käytettiin alkuperäisessä tapahtumassa, ja myös vastakirjauspäätili.</P>



6.  Luo tapahtumat merkinnöille, kuten maksuille ja koroille, jotka ovat tiliotteessa, mutta joita ei ole kirjattu Financeen. Kirjoita **Pankkitapahtuman tyyppi** ja asianmukaiset taloushallinnon dimensiot.

7.  Kun pankkitilin tapahtumat merkitään **Selvitetyt**-merkillä, jatkuvasti uudelleen laskettava **Täsmäyttämätön**-kentän summa lähenee nollaa. Kun kentän arvo lähenee nollaa, kirjaa täsmäytys sekä luomasi tapahtumat ja korjaukset valitsemalla **Täsmäytä tili**.
    
    Kun täsmäytys on kirjattu, sisällytettyjä tapahtumia ei voi muokata tai korjata eivätkä ne näy seuraavissa tilin täsmäytyksissä.

8.  Voit tarkastella pankkitapahtumia, joita ei ole vielä täsmäytetty, käyttämällä **Täsmäyttämättömät pankkitapahtumat** -raporttia. Jos haluat tarkastella pankkitilin tiliotetta, käytä **Tiliote**-raporttia.

## <a name="cancel-bank-statement-reconciliation"></a>Peruuta tiliotteen täsmäytys 

Peruuta tiliotteen täsmäytys -toiminnon avulla voit peruuttaa tiliotteen täsmäytyksen. Jos haluat käyttää tätä ominaisuutta, ota käyttöön **Peruuta tiliotteen täsmäytys** -ominaisuus **Toimintojen hallinta** -työtilassa. Sinun on myös otettava käyttöön **Salli tiliotteen muokkaus** -parametri. Voit tehdä tämän siirtymällä kohtaan **Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot > Pankkitilin täsmäytys**.
 
Tiliotteen täsmäytykset voidaan peruuttaa vain siinä aikajärjestyksessä, jossa ne on syötetty. Kun tiliotteen täsmäytys peruutetaan, uudet tapahtumat ja korjaukset peruutetaan ja kaikki muut tapahtumat merkitään täsmäyttämättömiksi.
 
Jos haluat peruuttaa tiliotteen täsmäytyksen, valitse tiliote ja valitse sitten **Tiliote > Peruuta pankkitilin täsmäytys**. Anna **Peruuta pankkitilin täsmäytys** -sivulla **Syykoodi**, **Syyn kommentti**ja **Peruutuspäivämäärä**. Aloita peruutus valitsemalla **OK**. Huomautus: tiliotteen peruutus päivämäärän on oltava tiliotteen päivämääränä tai sen jälkeen. Kun tiliotteen täsmäytys on peruutettu, tiliotteen **Peruutuspäivämäärä** -kenttään päivitetään annettu **Peruutuspäivämäärä**. Valitse **Tapahtumat**-painike, jos haluat tarkastella tapahtumia, joiden täsmäytys peruutettiin.
