---
title: "Valikoimien määrittäminen"
description: "Tässä artikkelissa kuvataan, mitä valikoimat ovat ja kerrotaan, kuinka voit määrittää valikoimia Microsoft Dynamics 365 for Operations - Retailissa."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 906fc6eb42eb54cb3a3d5621377f250f59de20d7
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-assortments"></a>Valikoimien määrittäminen

[!include[banner](includes/banner.md)]


Tässä artikkelissa kuvataan, mitä valikoimat ovat ja kerrotaan, kuinka voit määrittää valikoimia Microsoft Dynamics 365 for Operations - Retailissa.

Valikoima on kokoelma toisiinsa liittyviä tuotteita, jotka määritetään vähittäismyynnin kanavalle, kuten myymälälle tai verkkokaupalle. Voit käyttää valikoimia tunnistamaan tuotteet, jotka ovat myynnissä jokaisessa myymälässä. Valikoimaan voi sisältyä tuoteluokkia. Siispä kaikki tiettyyn luokkaan määritetyt tuotteet sisältyvät valikoimaan. Valikoimaan voi myös sisältyä tiettyjä tuotteita ja tuotevariantteja. Valikoiman määrittämällä voit määrittää tuhansia tuotteita vähittäismyynnin kanaviisi yhdellä kertaa juuri sellaisena yhdistelmänä, joka liikkeissäsi tarvitaan. Voit määrittää niin monta tuotevalikoimaa kuin on tarpeen. Kukin tuote voi kuulua yhteen tai useampaa valikoimaan, ja jokaisen valikoiman voi määrittää yhteen tai useampaan vähittäismyynnin kanavaan. Voit esimerkiksi määrittää yhden valikoiman, joka sisältää joukon perustuotteita. Tämä valikoima kuuluu kaikille myymälöille. Voit sitten määrittää toisen valikoiman, joka sisältää vain suuria urheiluvälineitä. Vain suuremmat myymäläsi saavat tämän valikoiman. Seuraavassa kaaviossa näkyy, kuinka tuotteet voi liittää valikoimiin, ja valikoimat voi liittää vähittäismyynnin kanaviin. ![Tuotevalikoimien suhteet](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Edellytykset
Ennen kuin voit määrittää valikoiman ja liittää sen vähittäismyynnin kanavaan, sinun on suoritettava seuraavat tehtävät.

| Tehtävä                              | Kuvaus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä vähittäismyynnin kanava.          | Vähittäismyynnin kanavia ovat myymälät, verkkokaupat ja online-kauppapaikat. Sinun on määritettävä vähintään yksi vähittäismyynnin kanava sekä kaupan asetukset. Määrittämällä valikoimat myymälöille tunnistat tuotteet, jotka ovat saatavilla tietystä myymälästä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Luo organisaatiohierarkia. | Kun olet määrittänyt organisaatiosi vähittäismyynnin kanavat, sinun on määritettävä vähittäismyynnin organisaatiohierarkia, joka vastaa vähittäismyynnin kanaviesi organisaatiorakennetta. Organisaatiohierarkiaa voidaan käyttää esimerkiksi valikoimissa, täydennyksissä ja raportoinnissa. Voit määrittää valikoimia myymäläryhmille lisäämällä vähittäismyynnin kanavia organisaatiohierarkiaan. Sen sijaan, että määrittäisit valikoiman erikseen kullekin myymälälle, voit määrittää valikoiman organisaation ylätason solmulle. Nyt, milloin tahansa lisäätkin uuden vähittäismyynnin kanavan organisaation ylätason solmuun, kyseinen kanava perii automaattisesti kaikki solmulle määritetyt valikoimat. Voit määrittää valikoimia ainoastaan vähittäismyynnin kanaville, jotka sisältyvät organisaatiohierarkiaan, jolle on määritetty **Vähittäismyyntivalikoima**-tarkoitus. |
| Määritä tuotteet.                  | Ennen kuin voit lisätä tuotteita valikoimaan, sinun on lisättävä tuotteet Microsoft Dynamics AX:ään. Voit lisätä tuotteet manuaalisesti tai voit tuoda ne toimittajalta. Kun olet lisännyt tuotteet, ne tulee vapauttaa yritykselle. Vain tuotteet, jotka on vapautettu yritykselle, voidaan tuoda vähittäismyyntikanavien saataville. Tuotteet, joita ei ole vielä vapautettu yrityksen käyttöön voidaan lisätä valikoimaan, ja valikoima voidaan hyväksyä. Vasta kun tuotteet on vapautettu yritykselle, voidaan ne tuoda vähittäismyyntikanavien saataville.                                                                                                                                                                                                                                                                                     |
| Määritä luokkahierarkia.      | Voit vähittäismyynnin tuotteita luodessasi ryhmitellä ja luokitella ne käyttämällä Microsoft Dynamics 365 for Operationsin luokkahierarkia-ominaisuutta. Voit luoda yhden ydinhierarkian, jonka avulla voit ryhmitellä ja luokitella kaikki vähittäismyyntikanaviesi kautta tarjoamasi tuotteet. Voit myös luoda erillisiä, täydentäviä luokkahierarkioita ryhmitelläksesi tai luokitellaksesi tuotteesi erityistarkoituksiin, kuten kampanjoihin tai valikoimiin. Luokkahierarkioiden avulla voit määrittää kaikki tietyn luokan tuotteet valikoimaan. Kaikki tuotteet, jotka lisätään valikoimaan sisältyvään luokkaan sisältyvät automaattisesti valikoimaan. Seuraavan kerran, kun vähittäismyynnin valikoiman ajastustyö suoritetaan, nämä tuotteet tulevat saataville vähittäismyynnin kanaviin, joihin valikoima on määritetty.                                            |

## <a name="setting-up-an-assortment"></a>Valikoiman määrittäminen
Kun olet määrittänyt edellytykset, voit luoda valikoiman ja määrittää sen vähittäismyynnin kanaville. Kun määrität valikoimaa, tee seuraavat tehtävät:

1.  Luo uusi valikoima tai kopioi aiemmin luotu valikoima.
2.  Valitse vähittäismyynnin kanavat tai vähittäismyynnin kanavien ylätason ryhmät, joita valikoima koskee.
3.  Lisää tuoteluokkia, yksittäisiä tuotteita tai tuotevariantteja valikoimaan. Voit sisällyttää kaikki tietyn luokan tuotteet tai ohittaa tietyt tuotteet valikoimaan kuuluvasta luokasta.
4.  Julkaise valikoima. Valikoiman ajastus suoritetaan automaattisesti, kun valikoima julkaistaan. Tämä prosessi luo tuoteluettelon. Kun tämä prosessi on valmis, tuotteet vapautuvat vähittäismyynnin kanaville, joille tuotevalikoima on määritetty. Jos julkaistuun valikoimaan tai sille määritettyihin vähittäismyynnin kanaviin tehdään muutoksia, valikoima on päivitettävä. Aja vähittäismyynnin valikoimien ajastustyö komentojonotyönä päivittääksesi valikoiman muutosten yhteydessä.





