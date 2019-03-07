---
title: Valikoimien määrittäminen
description: Tässä artikkelissa kuvataan, mikä valikoima on, ja kerrotaan, kuinka voit määrittää valikoimia Microsoft Dynamics 365 for Retailissa.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a9578a0784d4f4fbfca27ec4093a3f61d1068a47
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "314966"
---
# <a name="set-up-assortments"></a>Valikoimien määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, mikä valikoima on, ja kerrotaan, kuinka voit määrittää valikoimia Microsoft Dynamics 365 for Retailissa.

Valikoima on kokoelma toisiinsa liittyviä tuotteita, jotka määritetään vähittäismyynnin kanavalle, kuten myymälälle tai verkkokaupalle. Voit käyttää valikoimia tunnistamaan tuotteet, jotka ovat myynnissä jokaisessa myymälässä. Valikoimaan voi sisältyä tuoteluokkia. Siispä kaikki tiettyyn luokkaan määritetyt tuotteet sisältyvät valikoimaan. Valikoimaan voi myös sisältyä tiettyjä tuotteita ja tuotevariantteja. Valikoiman määrittämällä voit määrittää tuhansia tuotteita vähittäismyynnin kanaviisi yhdellä kertaa juuri sellaisena yhdistelmänä, joka liikkeissäsi tarvitaan. Voit määrittää niin monta tuotevalikoimaa kuin on tarpeen. Kukin tuote voi kuulua yhteen tai useampaa valikoimaan, ja jokaisen valikoiman voi määrittää yhteen tai useampaan vähittäismyynnin kanavaan. Voit esimerkiksi määrittää yhden valikoiman, joka sisältää joukon perustuotteita. Tämä valikoima kuuluu kaikille myymälöille. Voit sitten määrittää toisen valikoiman, joka sisältää vain suuria urheiluvälineitä. Vain suuremmat myymäläsi saavat tämän valikoiman. Seuraavassa kaaviossa näkyy, kuinka tuotteet voi liittää valikoimiin, ja valikoimat voi liittää vähittäismyynnin kanaviin.

![Tuotevalikoimien suhteet](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit määrittää valikoiman ja liittää sen vähittäismyynnin kanavaan, sinun on suoritettava seuraavat tehtävät.

| Tehtävä                              | Kuvaus |
|-----------------------------------|-------------|
| Määritä vähittäismyynnin kanava.          | Vähittäismyynnin kanavia ovat myymälät, verkkokaupat ja online-kauppapaikat. Sinun on määritettävä vähintään yksi vähittäismyynnin kanava sekä kaupan asetukset. Määrittämällä valikoimat myymälöille tunnistat tuotteet, jotka ovat saatavilla tietystä myymälästä. |
| Luo organisaatiohierarkia. | Kun olet määrittänyt organisaatiosi vähittäismyynnin kanavat, sinun on määritettävä vähittäismyynnin organisaatiohierarkia, joka vastaa vähittäismyynnin kanaviesi organisaatiorakennetta. Organisaatiohierarkiaa voidaan käyttää esimerkiksi valikoimissa, täydennyksissä ja raportoinnissa. Voit määrittää valikoimia myymäläryhmille lisäämällä vähittäismyynnin kanavia organisaatiohierarkiaan. Sen sijaan, että määrittäisit valikoiman erikseen kullekin myymälälle, voit määrittää valikoiman organisaation ylätason solmulle. Nyt, milloin tahansa lisäätkin uuden vähittäismyynnin kanavan organisaation ylätason solmuun, kyseinen kanava perii automaattisesti kaikki solmulle määritetyt valikoimat. Voit määrittää valikoimia ainoastaan vähittäismyynnin kanaville, jotka sisältyvät organisaatiohierarkiaan, jolle on määritetty **Vähittäismyyntivalikoima**-tarkoitus. |
| Määritä tuotteet.                  | Ennen kuin voit lisätä tuotteita valikoimaan, sinun on lisättävä tuotteet Microsoft Dynamics 365 for Retailiin. Voit lisätä tuotteet manuaalisesti tai voit tuoda ne toimittajalta. Kun olet lisännyt tuotteet, ne tulee vapauttaa yritykselle. Vain tuotteet, jotka on vapautettu yritykselle, voidaan tuoda vähittäismyyntikanavien saataville. Tuotteet, joita ei ole vielä vapautettu yrityksen käyttöön voidaan lisätä valikoimaan, ja valikoima voidaan hyväksyä. Vasta kun tuotteet on vapautettu yritykselle, voidaan ne tuoda vähittäismyyntikanavien saataville. |
| Määritä luokkahierarkia.      | Voit vähittäismyynnin tuotteita luodessasi ryhmitellä ja luokitella ne käyttämällä luokkahierarkia-ominaisuutta. Voit luoda yhden ydinhierarkian, jonka avulla voit ryhmitellä ja luokitella kaikki vähittäismyyntikanaviesi kautta tarjoamasi tuotteet. Voit myös luoda erillisiä, täydentäviä luokkahierarkioita ryhmitelläksesi tai luokitellaksesi tuotteesi erityistarkoituksiin, kuten kampanjoihin tai valikoimiin. Luokkahierarkioiden avulla voit määrittää kaikki tietyn luokan tuotteet valikoimaan. Kaikki tuotteet, jotka lisätään valikoimaan sisältyvään luokkaan sisältyvät automaattisesti valikoimaan. Seuraavan kerran, kun vähittäismyynnin valikoiman ajastustyö suoritetaan, nämä tuotteet tulevat saataville vähittäismyynnin kanaviin, joihin valikoima on määritetty. |

## <a name="setting-up-an-assortment"></a>Valikoiman määrittäminen

Kun olet määrittänyt edellytykset, voit luoda valikoiman ja määrittää sen vähittäismyynnin kanaville. Kun määrität valikoimaa, tee seuraavat tehtävät:

1. Luo uusi valikoima tai kopioi aiemmin luotu valikoima.
2. Valitse vähittäismyynnin kanavat tai vähittäismyynnin kanavien ylätason ryhmät, joita valikoima koskee.
3. Lisää tuoteluokkia, yksittäisiä tuotteita tai tuotevariantteja valikoimaan. Voit sisällyttää kaikki tietyn luokan tuotteet tai ohittaa tietyt tuotteet valikoimaan kuuluvasta luokasta.
4. Julkaise valikoima. Valikoiman ajastus suoritetaan automaattisesti, kun valikoima julkaistaan. Tämä prosessi luo tuoteluettelon. Kun tämä prosessi on valmis, tuotteet vapautuvat vähittäismyynnin kanaville, joille tuotevalikoima on määritetty. Jos julkaistuun valikoimaan tai sille määritettyihin vähittäismyynnin kanaviin tehdään muutoksia, valikoima on päivitettävä. Aja vähittäismyynnin valikoimien ajastustyö komentojonotyönä päivittääksesi valikoiman muutosten yhteydessä.
