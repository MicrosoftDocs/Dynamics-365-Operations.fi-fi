---
title: Työtilausten esittely
description: Tässä aiheessa on yleiskatsaus resurssien hallinnan työtilauksiin.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875638"
---
# <a name="introduction-to-work-orders"></a>Työtilausten esittely

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Työtilausten avulla hallitaan, annetaan tarvittavia tietoja ja rekisteröidään ylläpitotöiden kulutusta. Työtilaus voi sisältää yhden tai useita työtilaustöitä, ja yksi tai usea käyttöomaisuuserä voidaan liittää työtilaukseen. Kukin työtilausrivi määrittää käyttöomaisuuserälle ajoitetun kunnossapitotyön.

Työtilaukset voidaan luoda automaattisesti tai manuaalisesti:

- Automaattisesti käyttämällä **Ajoita ylläpitosuunnitelmat** -lomaketta kalenteriin perustuville ylläpitosuunnitelmille, joilla on määritetty "Luo automaattisesti".  

- Automaattisesti käyttämällä **Ajoita ylläpitokierrokset** -lomaketta ylläpitokierroksille, joilla on määritetty "Luo automaattisesti".  

- Luo ylläpitoaikataulusta, joka voi olla ennaltaehkäisevä kunnossapitotyö tai huoltopyyntö.  

- Luo työtilaus manuaalisesti.  

- Luo työtilaus kohdassa **Kaikki ylläpitopyynnöt** tai **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt**.

>[!NOTE]
>Samaan käyttöomaisuuserään liittyvät työtilaustyöt liittyvät samaan projektitunnukseen.

## <a name="all-work-orders"></a>Kaikki työtilaukset

Valitse **Resurssien hallinta** > **yhteiset** > **työtilaukset** > **Kaikki työtilaukset** avataksesi luettelon. **Kaikki työtilauksen** -luettelo sisältää kaikki työtilaukset ja siinä näkyy joitakin työtilaukseen liittyviä tietoja.

![Kuva 1](media/01-work-orders.png)

- Valitse **Resurssien hallinta** > **yhteiset** > **työtilaukset** >  **Aktiiviset työtilaukset** nähdäksesi aktiiviset työtilaukset listassa.

- Valitse **Resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Omat toiminnallisen sijainnin tytötilausten ylläpitotyöt** nahdaksesi luettelon työtilaustöistä, jotka sisältävät toiminnallisiin sijainteihin asennettuja resursseja, joihin olet suhteessa työntekijänä (määritetään kohdassa [Ylläpitotyöntekijät ja -työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md)).

- Valitse **Kaikki työtilaukset**-luettelon (ruudukkonäkymä) **Työtilaus** -sarakkeesta linkki, jos haluat tarkastella valitun tietueen Tiedot-näkymää. Avaa muokkausta varten napsauttamalla **Muokkaa**-painiketta.  

- Tiedot-näkymässä näkyvät työtilaukseen liittyvät yksityiskohtaiset tiedot.  

- Valitse Tiedot-näkymässä **Rivit** -linkki, jos haluat tarkastella työtilauksen työn tietoja tai valitse **Otsikko**-linkki, jos haluat nähdä työtilauksen tiedot.  

- Näytön oikealla puolella oleva pystysuuntainen **Aiheeseen liittyviä tietoja** -ruutu sisältää muita työtilaukseen liittyviä tietoja. Laajenna ruutu, jos haluat näyttää valitun työtilauksen liittyvät tiedot.  


![Kuva 2](media/02-work-orders.png)


Toimintoruudun painikkeet on järjestetty välilehtiin. Seuraavassa on lyhyt kuvaus yrityksen resurssien hallintaan liittyvistä painikkeista:



| Painikkeen nimi                     | Kuvaus                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Muokkaa                            | Muokkaa valittua työtilausta.                                                                                                                                                                                                                                           |
| Uusi                             | Luo uusi työtilaus.                                                                                                                                                                                                                                                  |
| Poista                          | Poista valittu työtilaus.                                                                                                                                                                                                                                         |
| Työtilauspooli                 | Lisää valittu työtilaus työtilauspooliin tai poista se työtilauspoolista.                                                                                                                                                                                           |
| Oikaisu                          | Muuta valittujen työtilausten odotettuja alkamis- ja loppumisaikoja, palvelutasoa, vastuullista huollon työntekijää tai vastuullista kunnossapitotyöntekijäryhmää.                                                                                                                                     |
| Tähän liittyvä työtilaus              | Luo uusi valittuun työtilaustyöhön liittyvä työtilaus. Tästä on hyötyä, jos haluat rekisteröidä ensisijaiset ja toissijaiset työtilaukset.                                                                                                                              |
| Kopioi työtilaus                 | Luo uusi työtilaus aiemmin luodun työtilauksen perusteella.                                                                                                                                                                                                                |
| Tapahtumahistoria                   | Katso työtilauksen kirjaushistoria.                                                                                                                                                                                                                |
| Työtilauksen ylläpitotyön huomautukset                           | Luo työtilaukseen kuvaus tai lisää huomautuksia tai muistiinpanoja. Aloita napsauttamalla **Lisää aikaleima** -painiketta, jolloin voit lisätä muistiinpanoon käyttäjänimesi ja aikaleiman. Huomautukset näkyvät **Työtilaus**-lomakkeen **Rivin tiedot** -pikavälilehden **Kuvaus**-välilehdessä. |
| Työkalut                           | Luo työtilaukseen tarvittavien työkalujen luettelo. työkalut määritetään resurssiena kohdassa **Organisaation hallinto** > **Yhteiset** > **Resurssit** > **Resurssit**.                                                                                                      |
| Ylläpidon tarkistuslista           | Näytä työtilaukseen liitetyn käyttöomaisuuserän tarkistusluettelo.                                                                                                                                                                                                              |
| Resurssin vika                     | Tarkastele tai rekisteröi käyttöomaisuus erän vikatietoja, joita käytetään vian hallinnassa.                                                                                                                                                                                        |
| Ylläpidon käyttökatko            | Määritä työtilauksen kunnossapitoseisokit.                                                                                                                                                                                                                               |
| Kunnon arviointi            | Rekisteröi työtilauksen kunnon arviointimittaukset.                                                                                                                                                                                                             |
| Resurssilaskurit                 | Luo tai tarkastele resurssin laskurirekisteröintejä.                                                                                                                                                                                                                     |
| Ennuste                        | Tarkastele tai luo työtilauksen ennusteita.                                                                                                                                                                                                                               |
| Kirjauskansiot                        | Tarkastele tai luo työtilausten kirjauskansioita. Kirjauskansion rivit voidaan kopioida ennusteista.                                                                                                                                                                                         |
| Projektitapahtumat            | Tarkastele kaikkia käyttöomaisuudelle luotuihin työtilauksiin liittyviä kirjattuja tapahtumia.                                                                                                                                                                                             |
| Päivitä työtilauksen tila                | Päivitä työtilauksen elinkaaren tila.                                                                                                                                                                                                                                                |
| Elinkaaren tilan loki                       | Loki, jossa näkyvät valitun työtilauksen elinkaaritilat.                                                                                                                                                                                                                   |
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


**Työtilaus**-välilehden painikkeiden **Projekti**-ryhmä liittyvät **Projektinhallinta ja kirjanpito** -moduulin ennusteisiin, kirjauskansioihin ja laskutukseen.

>[!NOTE]
>Työtilaukselle luodut ennusteet voidaan sisällyttää pääajoituksen suorittamiseen käyttämällä **Resurssienhallinnan parametrit** -lomakkeessa valittua ennustemallia.

