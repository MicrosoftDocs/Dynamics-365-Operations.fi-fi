---
title: Aaltomallit
description: Tässä ohjeaiheessa kuvataan ehdot, jotka määrittävät, käsitelläänkö aallot manuaalisesti vai automaattisesti, ja kuinka aallon käsittelyn yhteydessä varastolle luotu työ käsitellään.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: aca03e3fda4405fa6fe2b427a47066af5bb95b644b7f5b47d22736347208a8bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751622"
---
# <a name="wave-templates"></a>Aaltomallit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan ehdot, jotka määrittävät, käsitelläänkö aallot manuaalisesti vai automaattisesti, ja kuinka aallon käsittelyn yhteydessä varastolle luotu työ käsitellään. Voit määrittää ehdot asettamalla aaltomallit ja kyselyt, jotka vastaavat aaltoa myyntitilausten, tuotantotilausten ja kanbanien vapautettujen rivien kanssa.

## <a name="settings-for-wave-templates"></a>Aaltomallien asetukset

Määrittäessäsi wave-malli määritetään seuraavat:

- **Toimipaikka** ja **Varasto**, jolle malli luodaan.
- Tilaus, jossa mallit arvioidaan. Järjestys, jonka perusteella mallit täsmäytetään vapautettuihin riveihin myyntitilauksissa, tuotantotilauksissa ja kanbaneissa. Kun rivi vapautetaan, järjestelmä käyttää ensimmäistä aaltomallia, jonka perusteella rivi täyttää ehdot. Mitä laajemmat kriteerit, sitä todennäköisemmin rivi täyttää kriteerit, joten yksityiskohtaisimmat kriteerit täyttävät mallit pitäisi laittaa luettelon yläosaan. Järjestele malleja luettelossa toimintoruudun **Siirrä ylös**- ja **Siirrä alas** -painikkeilla.
- Kunkin mallin toimenpiteet. Aaltojen **menetelmät** suorittavat mallin luomia toimintoja, kuten esimerkiksi työn luonti tai jakaminen jokaiselle aaltomallin tyypille.
- Aallon määritteet (suodattimet), joita on sovellettava käytettävään aaltomalliin.

> [!NOTE]
> Tarvittaessa kehittäjä voi luoda muita menetelmiä. Voit tarkastella menetelmien kattavaa luetteloa **Aallon käsittelymallit** -sivulla.

Eräät asetukset kuvaavat strategisia päätöksiä aaltokäsittelylle seuraavasti:

- Jos mallia käytetään myyntitilauksien ja siirtotilauksien lähettämiseen tai käytettävien nimikkeiden siirtämiseksi tuotantoon, tuotantotilauksiin tai kanbaneihin.
- Jos aalto käsitellään manuaalisesti tai automaattisesti seuraavilla tavoilla:

  - **Manuaalinen käsittely** – rivi lisätään aalloksi ja varasto varataan, mutta sinun on kuitenkin Valittava **Käsittele** **Kaikki aallot** -luettelosivulla, jotta järjestelmä luo tilaukselle keräilytyön.
  - **Automaattinen käsittely** – voit automatisoida aallon käsittelyn osittain tai kokonaan. Jos olet automatisoinut aaltokäsittelyn kokonaan, luodaan aalto, joka sisältää myyntitilausrivin, tuotantotilausrivin tai kanban-rivin, kun myyntitilaus, tuotantotilaus tai kanban luodaan. Nimikkeet vähennetään käytettävissä olevasta varastosta ja keräilytyö luodaan. Jos voit automatisoida osittain aallon käsittelyn, voit määrittää arvot, jotka käynnistävät aallon käsittelyn. Voit esimerkiksi määrittää lähetyksille enimmäispainon, joka laukaisee aallon käsittelyn, kun aallon rivien kokonaispaino saavuttaa arvon.

- Jos määrität toimitukset avonaiselle aallolle. Esimerkiksi jos lupaat asiakkaille, että klo 12:00 mennessä määritetty tilaus toimitetaan 24 tunnin kuluessa, voit asettaa aaltomallin määrittämään automaattisesti tilausrivit avoimeen aaltoon klo 24:00 asti. Tällöin aalto käsitellään automaattisesti.

Kun aaltoa käsitellään, luodut keräilytyöt perustuvat varastolle määriteltyyn työmalliin ja sijaintidirektiiviin. Työmalli määrittää, kuinka keräilytyö luodaan, ja sijaintidirektiivi määrittää keräily- ja laittosijainnit.

## <a name="create-a-wave-template"></a>Luo aaltomalli

Määritä aaltomalli noudattamalla seuraavia ohjeita:

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Aallot** \> **Aaltomallit**.
1. Luo uusi aaltomalli valitsemalla **Uusi**.
1. Valitse  **Aaltomallin tyyppi**-kenttään jokin seuraavista vaihtoehdoista:

    - *Lähetys*: Käytä aaltomallia myyntitilausten ja siirtotilausten lähettämiseen.
    - *Tuotantotilaukset* – Käytä aaltomallia tuotantotilausten nimikkeiden siirtämiseen.
    - *Kanban* – Käytä aaltomallia kanban-tilausten nimikkeiden siirtämiseen.

1. Kirjoita aaltomallin nimi ja kuvaus **Aaltomallin nimi**- ja **Aaltomallin kuvaus** -kenttiin.

    > [!NOTE]
    > Jos varastolle luodaan useita malleja, numero **Aaltomallin järjestys**-kentässä ilmaisee järjestyksen, johon mallin sijainnin järjestyksessä, johon malleja käytetään, silloin kun mallin ehdot täyttyvät. Voit muuttaa mallien järjestystä valitsemalla **Siirrä ylös** tai **Siirrä alas**.

1. Valitse **Toimipaikka**- ja **Varasto**-kentistä toimipiste ja varasto, jolle aaltomalli luo aaltoja ja keräystyötä.
1. Jos haluat automatisoida aaltokäsittelyn, tee tarpeen mukaan seuraavat asetukset:

    - **Automatisoi aallon luonti** – Valitse arvoksi *Kyllä*, jos haluat luoda aallon automaattisesti, kun myyntitilaus, tuotantotilaus tai kanban vapautetaan varastoon.
    - **Määritä avoimiin aaltoihin** – Määritä arvoksi *Kyllä*, jos haluat määrittää rivejä automaattisesti avoimeen aaltoon, kun rivit vapautetaan. Rivit määritetään aaltoihin aaltomallin kyselysuodattimen perusteella.
    - **Käsittele aalto, kun se vapautetaan varastoon** – Määritä arvoksi *Kyllä*, jos haluat käsitellä aallon ja luoda työt automaattisesti, kun rivi vapautetaan varastoon.
    - **Käsittele aalto automaattisesti raja-arvossa** – Valitse arvoksi *Kyllä*, jos haluat käsitellä aallon automaattisesti, kun sen arvot saavuttavat **Aallon raja-arvot** -kenttäryhmässä painolle, lähetykselle ja riville määritetyt raja-arvot. Tämä asetus on käytettävissä vain, jos **Aaltomallin tyyppi** -kentässä on valittu *Lähetys*.
    - **Automatisoi aallon vapautus** – Määritä arvoksi *Kyllä*, jos haluat vapauttaa aallon automaattisesti. Keräilytyö luodaan ja määritetään mobiililaitteiden käytettäväksi.
    - **Automatisoi täydennystyön vapautus** – Jos määrität tämän vaihtoehdon arvoksi *Kyllä*, voit luoda täydennystyön tarpeen mukaan ja vapauttaa sen automaattisesti. Sinun on lisättävä täydennyksen aaltomenetelmä aaltomalliin ja luotava täydennysmalli, jonka tyyppi on *Aallon kysyntä*. Määritä täydennysmalli **Täydennysmallit**-sivulla. Tämä edellyttää, että lisäät täydennys-menetelmän aaltomalliin.
    - **Jatka aaltokäsittelyä, kun työn luonti epäonnistuu** – Kun arvo on *Kyllä*, järjestelmä käyttää tyhjää sijaintia, jos se ei voi varata varastoa sijaintidirektiivin ehdottamassa sijainnissa (esimerkiksi siksi, että varastoa ei ole enää saatavilla). Kun arvo on *Ei*, aalto epäonnistuu, jos järjestelmä ei voi varata varastoa.

1. Määritä **Aallon raja-arvot** -kenttäryhmä tarvittaessa:
    - **Aallon painon raja-arvo** – Anna suurin sallittu paino, jonka aalto voi sisältää.
    - **Lähetyksen raja-arvo** – Syötä lähetysten enimmäismäärä, joka voidaan sisällyttää aaltoon.
    - **Rivien raja-arvo** – Syötä rivien enimmäismäärä, joka voidaan sisällyttää aaltoon.

1. **Oletusarvot**-kenttäryhmässä valitse aaltomääritteet käytettäviksi aaltomallin lisäehtoina. Aaltomääritteet ovat käyttökelpoisia lisäkriteerien, kuten tietyn asiakkaan nimen, määrittämisessä aaltomalliin. Voit luoda nämä määritteet **Aallon määritteet**-sivulla. 

1. Määritä **Aallon ilmoituskäytäntö** käytännölle, jota haluat käyttää tätä mallia käyttäviin aaltoihin liittyvien ilmoitusten luomiseen. Esimerkiksi ilmoituskäytännöstä: [Aallon suorituksen ilmoitukset](wave-execution-notifications.md).

1. **Menetelmät**-pikavälilehden **Valitut menetelmät** -ruudussa näkyvät valitun aaltomallin tyypin menetelmät. Aaltojen menetelmät suorittavat mallin luomia toimintoja, kuten esimerkiksi työn luonti tai jakaminen. Näihin toimintoihin viitataan myös nimellä aaltovaiheet. Aallön menetelmät on määritetty ennalta jokaiselle aaltomallin tyypille. Et voi poistaa ennalta määritettyjä aaltomenetelmiä, mutta voit kuitenkin järjestää menetelmät uudelleen ja lisätä muita menetelmiä. Esimerkiksi jos olet luomassa aaltomallia toimitukselle, voit lisätä menetelmiä täydentämiselle ja konttienpakkaukselle. Aallon konttiin pakkaus voidaan lisätä aaltomenetelmien järjestykseen määrittämään aaltomallilla käsiteltyjen rivien konttiin pakkaus. Voit lisätä lisämenetelmän seuraavasti:

    - Valitse menetelmä **Jäljellä olevat menetelmät** -ruudusta **vasen** nuoli lisätäksesi sen **Valitut menetelmät** -ruutuun.
    - Jos haluat muuttaa järjestystä, valitse menetelmä ja valitse sitten **Ylös-** tai **Alas**-nuoli.

    > [!NOTE]
    > Kun lisäät menetelmän, se tulee näkyviin automaattisesti tarvittavissa kohteissa vaiheketjussa.

1. Jos haluat määrittää kyselyn, joka vastaa vapautettuja rivejä asianmukaisessa aallossa, valitse toimintoruudusta **Muokkaa kyselyä**.
1. Tarkasta, että aaltomallin asetukset ovat kelvollisia valitsemalla **Tarkista malli**.
