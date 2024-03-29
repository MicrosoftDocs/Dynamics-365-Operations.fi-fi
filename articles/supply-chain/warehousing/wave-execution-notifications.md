---
title: Aallon suoritusilmoitukset
description: Tässä artikkelissa käsitellään aallon suoritusilmoituksia ja niiden määrittämistä.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: a6a554965c11eea3b4fa53fe4dbc4bac04624026
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336572"
---
# <a name="wave-execution-notifications"></a>Aallon suoritusilmoitukset

[!include [banner](../includes/banner.md)]

*Aallon suoritusilmoitukset* -ominaisuus käyttää liiketoimintatapahtumia ja toimintokeskusta aaltojen suorittamiseen liittyvien ilmoitusten toimittamiseen. Sen avulla voit määrittää ilmoituksia tuottavien tapahtumien tyypit, niitä luovat varastot ja ne vastaanottavat käyttäjät.

Siirtymispalkin oikeassa sivussa oleva **Näytä viestit** -painike (kellosymboli) ilmaisee, milloin toimintokeskussanoma on nykyisen käyttäjän käytettävissä. Käyttäjä voi avata toimintokeskuksen ja tarkastella viestejä valitsemalla **Näytä viestit** -painikkeen.

Liiketoimintatapahtumat tapahtuvat, kun liiketoimintaprosesseja suoritetaan. Liiketoimintaprosessit koostuvat tehtävistä. Liiketoimintaprosessin aikana siihen osallistuvat käyttäjät suorittavat liiketoimintatoimintoja näiden tehtävien suorittamiseksi. Liiketoimintatapahtumat antavat mekanismin, jonka avulla ulkoiset järjestelmät saavat ilmoituksia talous- ja toimintosovelluksista. Tällä tavoin järjestelmät voivat suorittaa liiketoimintatoimintoja vastauksena liiketoimintatapahtumiin. Lisätietoja on kohdassa [Liiketoimintatapahtumien yleiskatsaus](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-the-wave-execution-notifications-feature-on-or-off"></a>Aallon suoritusilmoitukset -toiminnon ottaminen käyttöön tai pois käytöstä

Jos haluat käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Supply Chain Managementin versiosta 10.0.29 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.29, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Aallon suoritusilmoitukset* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Skenaario: Aallon eräsuorituksen ilmoitusten lähettäminen toimintokeskukseen

Tässä skenaariossa näkyy päästä päähän -työnkulku ilmoitusten lähettämiseen aallon eräsuorituksen virheist tietylle roolille toimintokeskuksen kautta.

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tämän skenaarion käyttäminen edellyttää, että demotiedot on asennettu ja että **USMF**-yritys on valittu.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Varmista, että aallot suoritetaan erätilassa

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä **Aallon käsittely** -pikavälilehdessä **Aallon käsittelyn eräryhmä** -arvoksi *Kyllä*.

> [!NOTE]
> Jos haluat poistaa aallon eräsuorituksen ilmoitukset käytöstä, määritä **Poista aallon käsittelyn eräilmoitukset käytöstä** -asetuksen arvoksi *Kyllä*.

### <a name="configure-a-wave-notification-policy"></a>Aallon ilmoituskäytännön määrittäminen

Aallon ilmoituskäytännöt määrittävät lähetetyt ilmoitustyypit ja käyttäjät, joille ilmoitetaan.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon ilmoituskäytännöt**.
1. Luo tietue, jossa on seuraavat asetukset:

    - **Aallon ilmoituskäytäntö:** *24BatchError*
    - **Kuvaus:** *Varaston 24 aallon erävirhe*
    - **Lähetä ilmoitus:** *Vain virhe*
    - **Roolille:** *Järjestelmänvalvojan*

        > [!NOTE]
        > Koska tässä skenaariossa käytetään esittelytietoja, *Järjestelmänvalvoja*-rooli valitaan yksinkertaisuuden vuoksi. Koska olet kirjautuneena järjestelmänvalvojana, saat ilmoitukset. Käytännössä kannattaa kuitenkin yleensä valita tarkempi rooli, jos haluat ilmoittaa aallon eräsuorituksen virheistä, kuten *Varaston esimies* -rooli.

1. Valitse toimintoruudussa **Tallenna**.

### <a name="configure-a-wave-template"></a>Aaltomallin määrittäminen

Aaltomallin avulla tietyt aaltomenetelmien esiintymät voidaan linkittää vastaavaan aallon etikettimalleihin.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Määritä luetteloruudussa **Aaltomallin tyyppi** -kentän arvoksi *Toimitus* ja valitse sitten varastolle 24 *24 Shipping Default* -aaltomalli.
1. Määritä **Yleiset**-pikavälilehden **Aallon ilmoituskäytäntö** -kentän arvoksi *24BatchError*.

### <a name="configure-a-work-template"></a>Työmallin määrittäminen

Työmalleja käytetään aaltojen suorittamisen aikana työn luomiseen. Tässä skenaariossa aallon suorittamisen pitäisi aiheuttaa virhe. Määrittämällä työmallikyselyn käyttämään olematonta varastoa varmistat, että aaltojen suorittaminen epäonnistuu, ja siksi ilmoitus lähetetään.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Määritä luetteloruudussa **Työmallin tyyppi** -kentän arvoksi *Myyntitilaukset* ja valitse sitten varastolle 24 *24 SO Stage* -työmalli.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Muokkaa kyselyeditorin valintaikkunan **Alue**-välilehdessä seuraavaa riviä (tai lisää se, jos sitä ei ole):

    - **Taulukko:** *Väliaikaiset työtapahtumat*
    - **Johdettu taulukko:** *Väliaikaiset työtapahtumat*
    - **Kenttä:** *Varasto*
    - **Ehdot:** Muuta arvosta *24* arvoon *Virhe*.

1. Valitse **OK** ja vahvista muutos.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Myyntitilauksen luominen ja sen vapauttaminen varastoon

1. Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.
1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Varasto**: *24*

1. Lisää **Myyntitilausrivit**-pikavälilehdessä myyntitilausrivi, jonka asetukset ovat seuraavat:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *10*

    > [!NOTE]
    > Nämä nimikkeet ja määrät ovat vain esimerkkejä. Määritetyssä varastossa on oltava riittävästi saldoa.

1. Kun uusi rivi on edelleen valittuna **Myyntitilausrivit**-pikavälilehdessä, valitse työnkalurivillä **Varasto \> Varaus**.
1. Valitse **Varaus**-sivun toimintoruudussa kohta **Varaa erä**. Sulje sitten sivu.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

### <a name="notifications-from-wave-batch-job-execution"></a>Ilmoitukset aallon erätyön suorituksesta

Liiketoimintatapahtumien määritysten mukaan saat lopulta ilmoituksen aallon suorittamisen epäonnistumisesta. Toimintokeskuksen sanoma muistuttaa seuraavaa esimerkkiä ja sisältää linkin epäonnistuneeseen aaltoon.

> **Virhe aallon suorituksen aikana**  
> Virhe suoritettavissa aaltoa USMF-000000001.  
> Viimeiset viestit: Töitä ei luotu aallolle USMF-000000001.
>
> **TILA**  
> Käytössä
>
> Avoimen aallon tiedot

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

