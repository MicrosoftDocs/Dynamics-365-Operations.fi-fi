---
title: Aaltokäsittelyn konfiguroinnin esimerkki
description: Tässä artikkelissa kuvataan esimerkki ehdoista, jotka määrittävät mitä töitä luodaan aallon käsittelyn yhteydessä varastolle ja käsitelläänkö aallot manuaalisesti vai automaattisesti.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a8c088f8726573e4b1fcad1944676547391a9bf
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219625"
---
# <a name="configure-wave-processing-example"></a>Aaltokäsittelyn konfiguroinnin esimerkki

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan esimerkki ehdoista, jotka määrittävät mitä töitä luodaan aallon käsittelyn yhteydessä varastolle ja käsitelläänkö aallot manuaalisesti vai automaattisesti. Voit määrittää ehdot asettamalla aaltomallit ja kyselyt, jotka vastaavat aaltoa myyntitilausten, tuotantotilausten ja kanban-tilausten vapautettujen rivien kanssa.

## <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen aloittamista.

## <a name="example-scenario-configure-wave-processing"></a>Esimerkkiskenaario: aaltokäsittelyn konfigurointi

Tässä esimerkissä tutustutaan moniin eri asetuksiin, jotka vaikuttavat aaltojen luontiin, täyttämiseen, käsittelemiseen ja vapauttamiseen.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Aallot > Aaltomallit**.
1. Valitse **Uusi**.
1. Syötä **Aaltomallin nimi** -kenttään arvo. Aaltomallia määrittäessäsi voit määrittää järjestyksen, jossa mallit sovitetaan vapautettuihin myyntitilausten, tuotantotilausten tai kanbanien riveihin. Kun rivi on vapautettu varastoon tai tuotantoon, siinä käytetään ensimmäistä ehtoja vastaavaa aaltomallia. Suosittelemme, että sijoitat tarkimmin määritellyt kriteerit sisältävän mallit luettelon alkuun. Mitä laajempi ehto on, sitä todennäköisemmin rivi täyttää ehdon, ja tämä saattaa johtaa rivien määrittämisen väärään aaltoon.  
1. Kirjoita **Aaltomallin kuvaus** -kenttään arvo.
1. Syötä tai valitse arvo **Toimipaikka**-kenttään. Jos käytössä on USMF, valitse toimipaikka 2.  
1. Anna tai valitse **Varasto**-kentässä arvo. Jos käytössä on USMF, voit valita varaston 24.  
1. Aseta **Automatisoi aallon luonti** -kentän arvoksi **Kyllä**. Valitse tämä vaihtoehto, jos haluat luoda aallon automaattisesti, kun myyntitilaus, tuotantotilaus tai kanban vapautetaan varastoon.  
1. Aseta **Käsittele aalto, kun se vapautetaan varastoon** -asetuksen arvoksi **Kyllä**. Valitse tämä vaihtoehto, jos haluat käsitellä automaattisesti aallon ja luoda työn, kun rivi vapautetaan varastoon.  
1. Aseta **Automatisoi aallon vapautus** -asetuksen arvoksi **Kyllä**. Valitse tämä vaihtoehto, kun haluat vapauttaa aallon automaattisesti. Keräilytyö luodaan ja määritetään mobiililaitteiden käytettäväksi.  
1. Aseta **Määritä avoimiin aaltoihin** -asetuksen arvoksi **Kyllä**. Rivit määritetään aaltoihin aaltomallin kyselysuodattimen perusteella.  
1. Aseta **Käsittele aalto automaattisesti raja-arvossa** -asetuksen arvoksi **Kyllä**. Valitse tämä vaihtoehto, jos haluat käsitellä aallon automaattisesti, kun sen arvot saavuttavat **Aallon raja-arvot** -kenttäryhmässä painolle, lähetykselle ja riville määritetyt raja-arvot. Tämä vaihtoehto on käytettävissä vain, jos **Aaltomallin tyyppi** -kentässä on valittu **Lähetys**.  
1. Aseta **Automatisoi täydennystyön vapautus** -asetuksen arvoksi **Kyllä**. Valitsemalla tämän vaihtoehdon voit luoda täydennystyön tarpeen mukaan ja vapauttaa sen automaattisesti. Sinun on lisättävä täydennyksen aaltomenetelmä aaltomalliin ja luotava täydennysmalli, jonka tyyppi on **Aallon kysyntä**.  
1. Arkistoidun **Oletusarvo**-ryhmän asetuksien avulla voit liittää aallon määritteitä. Aaltomääritteet toimivat suodattimina rajoittaen aaltoa käyttäviä nimikkeitä. Voit esimerkiksi määrittää nimikeryhmän.  
1. Laajenna **Menetelmät**-osa ja määritä aaltomallin toiminnot. Aaltomallimenetelmien avulla voit ohjata tehtäväsarjaa, jonka kukin aalto käy läpi käsittelyn aikana. Sinulla voi esimerkiksi olla menetelmä aallon täydentämiseen. Kun lisäät menetelmän, se tulee näkyviin automaattisesti tarvittavissa kohteissa vaiheketjussa. Jos olet asettanut **Automatisoi täydennystyön vapautus** -asetuksen arvoksi **Kyllä**, täydennysmenetelmä on lisättävä tähän.  
1. Valitse **Tallenna**.
1. Sulje sivu.
1. Valitse **Varastonhallinta > Asetukset > Varastonhallinnan parametrit**.
1. Laajenna **Aallon käsittely** -osa.
1. Anna tai valitse arvo **Aallon käsittelyn eräryhmä** -kenttään.
1. Aseta **Aallon käsittelyn eräryhmä** -asetuksen arvoksi **Kyllä**.
1. Anna **Odota lukitusta (ms)** -kenttään numero. Kirjoita millisekunteina aika, jonka kohdistusvaihe odottaa järjestelmäresurssia, joka on toisen kohdistusvaiheen lukitsema. Kun tämä aika ylitetään, aaltoa ei käsitellä ja virhesanoma tulee näkyviin.  
1. Valitse **Tallenna**.
1. Sulje sivu.
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Tuotannonhallinta > Asetukset > Tuotannonhallinnan parametrit**.
1. Valitse vaihtoehto **Vapauta varastoon** -kentässä.

    Myynti- ja kanbantilauksille inventaario tulee varata ennen kuin tilaus viedään varastolle. Muussa tapauksessa tietyn kohdistuksen rivejä ei voi käsitellä aallossa. Tuotantotilauksille on myös mahdollista valita **Salli osittainen varaaminen**. Tämä on hyödyllistä esimerkiksi silloin, kun sinulla on tuotannon käynnistämiseen tarvittavat materiaalit ja voit odottaa, kunnes muut materiaalit ovat käytettävissä saattaaksesi prosessin loppuun. Jos valitset tämän vaihtoehdon, pitää vapautus varastoprosessiin toistaa manuaalisesti, kun muut materiaalit tulevat käyttöön.
1. Sulje sivu.

## <a name="additional-resources"></a>Lisäresurssit

- [Aaltojen luominen ja käsittely](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
