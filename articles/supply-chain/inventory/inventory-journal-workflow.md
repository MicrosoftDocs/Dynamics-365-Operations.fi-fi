---
title: Varastokirjauskansion hyväksyntätyönkulut
description: Tässä ohjeaiheessa käsitellään varastokirjauskansioiden hyväksyntätyönkulut määritetään ja miten niitä käytetään erityyppisten varastotilannetapahtumien kirjaamisessa. Varastokirjauskansion työnkulkujen avulla voit varmistaa, että vain hyväksytyt varastokirjauskansiot voidaan kirjata tapahtumille.
author: sherry-zheng
manager: tfehr
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 596182dfd7430e4d1e35ffebb795fbcf98d45e33
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247907"
---
# <a name="inventory-journal-approval-workflows"></a>Varastokirjauskansion hyväksyntätyönkulut

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten varastokirjauskansion hyväksyntätyönkulkuja käytetään varastotilannetapahtumien eri tyypeissä, kuten varasto-otoissa ja -vastaanotoissa, varaston siirroissa, tuoterakenteissa ja fyysisen varaston täsmäytyksessä. Varastokirjauskansion työnkulkujen avulla voit varmistaa, että vain hyväksytyt varastokirjauskansiot voidaan kirjata tapahtumille.

> [!NOTE]
> Varastokirjauskansion hyväksymistyönkulkuja käytetään vain varastonhallintamoduulin avulla tallennettuihin tapahtumiin. Ne eivät toimi varastonhallintamoduulista käynnistettyjen varastokirjauskansioiden kanssa.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Varastokirjauskansion hyväksyntätyönkulut -toiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Varastokirjauskansion hyväksyntätyönkulku*

## <a name="create-your-inventory-journal-approval-workflows"></a>Varastokirjauskansion hyväksyntätyönkulun luominen

Jos haluat määrittää tämän toiminnon, sinun on luotava työnkulku kullekin hallittavalle varastokirjauskansiotyypille. Koska eri varastokirjauskansiotyypeillä on erilaiset hyväksyntähierarkiat ja työnkulun vaiheet, voit määrittää jokaiselle varastokirjauskansiotyypille yksilöllisen työnkulun.

Työnkulut tukevat versionhallintaa. Kullakin on työnkulkutunnus ja aktiivinen versio. Voit halutessasi aktivoida jokaisen uuden työnkulkuversion heti luonnin yhteydessä tai pitää sen poissa käytöstä. Jos tarvitset eri työnkulkuja samalle kirjauskansiotyypille, luo useita työnkulkuja kyseiselle kirjauskansiotyypille. Määritä sitten kukin näistä eri kirjauskansion nimelle, joka käyttää kyseistä tyyppiä.

Voit luoda varastokirjauskansion hyväksyntätyönkulun seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset\> Varastonhallinnan työnkulut**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse varastokirjauskansiotyyppi, jolle haluat määrittää työnkulun seuraavasti:
    - **Varaston tunnisteiden inventoinnin kirjauskansio**
    - **Varaston omistajuuden muutoksen kirjauskansio**
    - **Varaston siirtokirjauskansio**
    - **Varastosiirron kirjauskansio**
    - **Varaston inventoinnin kirjauskansio**
    - **Varaston tuoterakenteen kirjauskansio**
    - **Varaston oikaisukirjauskansio**

    ![Luo työnkulku -valintaikkuna](media/journal-workflow-create-workflow.png "Luo työnkulku -valintaikkuna")

1. Työnkulkueditorisovellus käynnistyy koneessa. (Sinua voidaan pyytää hyväksymään tämä toiminto.) Sen avulla voit suunnitella työnkulun tarpeen mukaan. Lisätietoja työnkulkueditorin käyttämisestä on kohdassa [Työnkulkujärjestelmän yleiskatsaus](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Kun olet tallentanut ja sulkenut työnkulkueditorisovelluksen, sinun on määritettävä, aktivoidaanko tämä työnkulkuversio vai pidetäänkö se passiivisena.

> [!NOTE]
> Työnkulut sisältävät versionhallinnan, joten voit tarkastella luotujen versioiden luetteloa ja valita, kumpi niistä on aktiivinen. Jos haluat tarkastella käytettävissä olevien versioiden luetteloa ja valita aktivoitavan version, valitse työnkulku **Varastonhallinnan työnkulut** -sivulla. Avaa toimintoruudun **Työnkulku**-välilehti ja valitse **Versiot**-kohta. Vain yksi versio voi olla aktiivinen kerralla kullakin työnkulun tunnuksella.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Hyväksyntätyönkulkujen määrittäminen varastokirjauskansion nimiin

Seuraava vaihe on määrittää varastokirjauskansion työnkulku kullekin varastokirjauskansion nimelle. Voit määrittää kullekin varastokirjaus kansiotyypille useita varastokirjauskansioiden nimiä.

Voit liittää varastokirjauskansion työnkulun varastokirjauskansion nimeen seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Kirjauskansioiden nimet \> Varasto**.
1. Valitse luettelosarakkeesta kirjauskansion nimi ja avaa sen asetussivu.
1. Määritä **Yleinen**-pikavälilehden **Hyväksyntätyönkulku**-asetukseksi **Kyllä**. Jos järjestelmä pyytää vahvistamaan toiminnon, valitse **Kyllä**.

    ![Työnkulun liittäminen kirjauskansion nimeen](media/journal-workflow-journal-name.png "Työnkulun liittäminen kirjauskansion nimeen")

1. Avaa avattava **Työnkulku**-luettelo ja valitse soveltuva työnkulku. Luettelossa näkyvät kaikki aktiiviset työnkulut, jotka olet luonut käyttämällä työnkulkueditorisovellusta.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Varastokirjauskansion luominen ja lähettäminen hyväksyttäväksi

Kun olet liittänyt varastokirjauskansion nimen sen vastaavaan varastokirjauskansion hyväksyntätyönkulkuun, voit luoda uusia varastokirjauskansioita, jotka käyttävät tätä nimeä- Tämän jälkeen voit lähettää nämä kirjauskansiot hyväksyttäväksi kyseisen työnkulun avulla. Et voi kirjata varastokirjauskansiota, ennen kuin työnkulussa määritetyt hyväksyjät ovat hyväksyneet sen.

1. Laajenna siirtymisruudussa kohta **Varastonhallinta \> Kirjauskansioviennit \> Nimikkeet** ja valitse sitten varastokirjauskansion tyyppi.
1. Valitse **Uusi**, jos haluat luoda uuden kirjauskansion valitusta tyypistä.
1. Näyttöön avautuu **Luo varastokirjauskansio** -valintaikkuna. Täytä lomake tarvittaessa ja valitse **OK**, jos haluat tallentaa kirjauskansion.
1. Viimeistele kirjauskansio tarpeen mukaan.
1. Kun luot tai avaat varastokirjauskansion, johon on liitetty hyväksyntätyönkulku, **Työnkulku**-painike on aktiivinen toimintoruudussa. Kun olet valmis lähettämään kirjauskansion hyväksyttäväksi, valitse **Työnkulku**-painike ja avaa avattava valintaikkuna. Valitse lopuksi **Lähetä**. Tämän jälkeen hyväksyntäpyyntö reititetään asiaankuuluvalle hyväksyjälle, joka saa hälytyksen työnkulkua varten konfiguroidun ilmoitusmenetelmän avulla.

    ![Lähetä kirjauskansio hyväksyttäväksi](media/journal-workflow-inventory-journal.png "Lähetä kirjauskansio hyväksyttäväksi")

Voit peruuttaa hyväksyntäpyynnön avaamalla asiaankuuluvan kirjauskansion, valitsemalla **Työnkulku**-painikkeen ja valitsemalla sitten **Peruuta**. Tämä nollaa työnkulun.

Kun kirjauskansio on hyväksytty, pystyt kirjaamaan sen. Voit kirjata kirjauskansion valitsemalla **Kirjaa** toimintoruudussa. Jos **Kirjaa**-painike ei ole aktiivinen, kirjauskansiota ei ole vielä hyväksytty.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Varastokirjauskansion hyväksymispyyntöön vastaaminen

Jos olet hyväksyjä, sinun pitäisi saada sanoma aina, kun hyväksyntää tarvitaan (määritetty työnkulussa). Tämän jälkeen voit hyväksyä tai hylätä kirjauskansion hyväksymispyynnön tekemällä seuraavat toiminnot:

1. Laajenna siirtymisruudussa kohta **Varastonhallinta \> Kirjauskansioviennit \> Nimikkeet** ja valitse sitten varastokirjauskansion tyyppi.
1. Avaa haluamasi kirjauskansio ja tarkista se.
1. Valitse **Työnkulku**-painike toimintoruudussa ja avaa avattava valintaikkuna. Valitse jokin seuraavista:
    - **Hyväksy** - Pyynnön hyväksyminen.
    - **Hylkää** - Pyynnön hylkääminen.
    - **Lisää \> Pyydä muutosta** - Voit lähettää pyytäjälle viestin, jossa pyydät tätä muuttamaan jotain tiettyä, ja lähettää uudelleen.
    - **Lisää \> Delegoi** - Hyväksynnän delegoiminen toiselle käyttäjälle.
    - **Lisää \> Peruuta** - Peruuta hyväksyntäpyyntö (nollaa työnkulun).
    - **Lisää \> Työnkulkuhistoria** - Tämän hyväksyntätyönkulun tähänastisen historian katselu.

## <a name="review-the-approval-history"></a>Hyväksymishistorian tarkistaminen

Muuntyyppisissä työnkuluissa voit käyttää **Työnkulkuhistoria**-sivua ja katsoa minkä tahansa kirjauskansion hyväksyntätyönkulun historian.

Voit tarkastella kirjauskansion työnkulkuhistoriaa seuraavasti:

1. Laajenna siirtymisruudussa kohta **Varastonhallinta \> Kirjauskansioviennit \> Nimikkeet** ja valitse sitten varastokirjauskansion tyyppi.
1. Avaa asiaankuuluva kirjauskansio.
1. Valitse **Työnkulku**-painike toimintoruudussa ja avaa avattava valintaikkuna. Valitse **Työnkulkuhistoria**. Lisätietoja on kohdassa [Työnkulkuhistorian tarkasteleminen](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]