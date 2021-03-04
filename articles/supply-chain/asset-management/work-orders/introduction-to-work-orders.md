---
title: Työtilausten esittely
description: Tässä aiheessa on yleiskatsaus resurssien hallinnan työtilauksiin.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7997b4b9521b43e1e00cfa22f9df12a29582455a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426894"
---
# <a name="introduction-to-work-orders"></a>Työtilausten esittely

[!include [banner](../../includes/banner.md)]



Työtilausten avulla hallitaan, annetaan tarvittavia tietoja ja rekisteröidään ylläpitotöiden kulutusta. Työtilaus voi sisältää yhden tai useita työtilaustöitä, ja yksi tai usea käyttöomaisuuserä voidaan liittää työtilaukseen. Kukin työtilaustehtävä määrittää käyttöomaisuuserälle ajoitetun kunnossapitotyön.

Työtilauksia voidaan luoda seuraavin tavoin:

- Automaattisesti käyttämällä [Ajoita ylläpitosuunnitelmat](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md) -lomaketta kalenteriin perustuvilla ylläpitosuunnitelmilla, joilla "Luo automaattisesti" -asetus on käytössä.

- Automaattisesti käyttämällä [Ajoita ylläpitokierrokset](../preventive-and-reactive-maintenance/maintenance-rounds.md) -lomaketta kalenteriin perustuvilla ylläpitokierroksilla, joilla "Luo automaattisesti" -asetus on käytössä.

- Ennaltaehkäisevien kunnossapitotöiden tai huoltopyyntöjen osalta [Ylläpitoaikataulu](../preventive-and-reactive-maintenance/maintenance-schedule.md).

- Manuaalisesti

- Sivulta **Kaikki ylläpitopyynnöt**, **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt**.

>[!NOTE]
>Samaan käyttöomaisuuserään liittyvät työtilaustyöt liittyvät samaan projektitunnukseen.

## <a name="all-work-orders"></a>Kaikki työtilaukset

Valitse **Resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** avataksesi **Kaikki työtilaukset** -luettelosivun. Tällä sivulla näkyvät kaikki työtilaukset ja osa niihin liittyvistä tiedoista.

Seuraavassa kuvassa on esimerkki **Kaikki työtilaukset** -luettelosivusta.

![Kuva 1](media/01-work-orders.png)

Valitse **Resurssien hallinta** > **Yhteiset** > **Työtilaukset** >  **Aktiiviset työtilaukset** nähdäksesi luettelon vain aktiivisista työtilauksista. 

Nähdäksesi luettelon työtilaustehtävistä, jotka sisältävät toiminnallisiin sijainteihin asennettuja resursseja, joihin sinä liityt työntekijänä, valitse **Resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Omat toiminnallisen sijainnin työtilausten ylläpitotyöt**. (Työntekijöiden ja toiminnallisten sijaintien välinen suhde määritetään **Työntekijät**-sivulla. Lisätietoja on kohdassa [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).)

Voit käyttää **Kaikki työtilaukset** -sivua esimerkiksi seuraavilla tavoilla:

- Valitse ruudukkonäkymässä sarakkeen **Työtilaus** linkki nähdäksesi valitun tietueen tietonäkymän. Valitsemalla **Muokkaa** tietue avautuu muokattavaksi.

- Tietonäkymässä näet yksityiskohtaisia työtilaukseen liittyviä tietoja.  

- Valitse tietonäkymässä **Rivit** -välilehti, jos haluat tarkastella työtilaustehtävän tietoja, tai valitse **Otsikko**-välilehti, jos haluat tarkastella työtilauksen tietoja.  

- Laajenna **Aiheeseen liittyviä tietoja** -ruutu sivun oikeassa laidassa saadaksesi lisää valittuun työtilaukseen liittyviä tietoja.

Seuraavassa kuvassa on esimerkki **Kaikki työtilaukset** -tietonäkymästä.

![Kuva 2](media/02-work-orders.png)


Toimintoruudun painikkeet on järjestetty välilehtiin. Seuraavassa taulukossa kuvataan lyhyesti resurssien hallintaan liittyvät painikkeet:



| Painikkeen nimi                     | Kuvaus                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Muokkaa                            | Muokkaa valittua työtilausta.                                                                                                                                                                                                                                           |
| Uusi                             | Luo uusi työtilaus.                                                                                                                                                                                                                                                  |
| Delete-näppäin                          | Poista valittu työtilaus.                                                                                                                                                                                                                                         |
| Työtilauspooli                 | Lisää valittu työtilaus työtilauspooliin tai poista se työtilauspoolista.                                                                                                                                                                                           |
| Oikaisu                          | Muuta valittujen työtilausten odotettuja alkamis- ja loppumisaikoja, palvelutasoa, vastuullista huollon työntekijää tai vastuullista kunnossapitotyöntekijäryhmää.                                                                                                                                     |
| Tähän liittyvä työtilaus              | Luo uusi valittuun työtilaustyöhön liittyvä työtilaus. Tästä on hyötyä, jos haluat rekisteröidä ensisijaiset ja toissijaiset työtilaukset.                                                                                                                              |
| Kopioi työtilaus                 | Luo uusi työtilaus aiemmin luodun työtilauksen perusteella.                                                                                                                                                                                                               |
| Tapahtumahistoria                   | Avaa työtilauksen rekisteröintihistoria.                                                                                                                                                                                                                |
| Työtilauksen ylläpitotyön huomautukset                           | Luo työtilaukseen kuvaus tai lisää sitä koskevia huomautuksia tai muistiinpanoja. Aloita valitsemalla **Lisää aikaleima**, jolloin voit lisätä muistiinpanoon käyttäjänimesi ja aikaleiman. Muistiinpanot näkyvät **Työtilaus**-sivun **Rivitiedot**-pikavälilehden **Kuvaus**-välilehdessä.         |
| Työkalut                           | Luo työtilaukseen tarvittavien työkalujen luettelo. Työkalut määritetään resursseiksi kohdassa **Organisaation hallinto** > **Resurssit** > **Resurssit**.                                                                                                      |
| Ylläpidon tarkistuslista           | Näytä työtilaukseen liitetyn resurssin tarkistusluettelo.                                                                                                                                                                                                              |
| Resurssin vika                     | Avaa tai rekisteröi resurssin vikatiedot. Tätä tietoa käytetään vikojen hallinnassa.                                                                                                                                                                                      |
| Ylläpidon käyttökatko            | Määritä työtilauksen kunnossapitoseisokit.                                                                                                                                                                                                                               |
| Kunnon arviointi            | Rekisteröi työtilauksen kunnon arviointimittaukset.                                                                                                                                                                                                             |
| Resurssilaskurit                 | Luo tai tarkastele resurssin laskurirekisteröintejä.                                                                                                                                                                                                                     |
| Ennuste                        | Tarkastele tai luo työtilauksen ennusteita.                                                                                                                                                                                                                               |
| Kirjauskansiot                        | Tarkastele tai luo työtilausten kirjauskansioita. Kirjauskansion rivit voidaan kopioida ennusteista.                                                                                                                                                                                         |
| Projektitapahtumat            | Tarkastele kaikkia resurssille luotuihin työtilauksiin liittyviä kirjattuja tapahtumia.                                                                                                                                                                                             |
| Päivitä työtilauksen tila           | Päivitä työtilauksen elinkaaren tila.                                                                                                                                                                                                                                                |
| Elinkaaren tilan loki                      | Tarkastele lokia, joka näyttää valitun työtilauksen elinkaaritilat.                                                                                                                                                                                                                   |
| Resurssin tiedostot                | Näytä luettelo työtilaukseen liittyviin resursseihin liitetyistä asiakirjoista. Nämä asiakirjat määritetään kohdassa **Resurssien hallinta**  >  **Asetukset**  >  **Resurssin tiedostot**.                                                                                                 |
| Aikataulu                        | Ajoita valitut työtilaukset.                                                                                                                                                                                                                                      |
| Lähetys            | Ajoita valittu työtilaus yhdelle työntekijälle.                                                                                                                                                                                                                        |
| Poista aikataulu                 | Poista valitun työtilauksen ajoitus.                                                                                                                                                                                                                          |
| Ajoitetut työtilauksen ylläpitotyöt             | Avaa **Ajoitetut työtilauksen ylläpitotyöt** -luettelosivu.                                                                                                                                                                                                                             |
| Työtilauksen ostoehdotus | Avaa **Työtilauksen ostoehdotus** -luettelosivu.                                                                                                                                                                                                                 |
| Työtilaus osto             | Avaa **Työtilauksen osto** -luettelosivu.                                                                                                                                                                                                                             |
| Kustannusseuranta                    | Vertaa työtilauksen budjettikustannuksia ja todellisia kustannuksia.                                                                                                                                                                                                                |
| Tuntien hallinta                    | Vertaa työtilaksen ennustetunteja ja todellisia tunteja.                                                                                                                                                                                                                |
| Työtilausraportti               | Tulosta työtilausraportti.                                                                                                                                                                                                                                                |
| Työtilauksen kulutus          | Tulosta kulutusraportti.                                                                                                                                                                                                                                               |


Toimintoruudun **Työtilaus**-välilehden **Projekti**-ryhmän painikkeet liittyvät ennusteiden, kirjauskansioiden ja laskutuksen toimintoihin **Projektinhallinta ja kirjanpito** -moduulissa.

>[!NOTE]
>Voit lisätä työtilaukselle luotuja ennusteita suorittaessasi pääajoitusta käyttämällä ennustemallia, joka on valittu **Resurssienhallinnan parametrit** -sivulla.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]