---
title: Tuotannon varianssien yleiset lähteet
description: Tässä artikkelissa selitetään tyypillisiä tuotannon varianssin tyyppien lähteitä.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b0f7a66c00540216887c7913e7f094c819b693a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673995"
---
# <a name="common-sources-of-production-variances"></a>Tuotannon varianssien yleiset lähteet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa selitetään tyypillisiä tuotannon varianssin tyyppien lähteitä. 

Seuraavassa on joitakin tyypillisiä **eräkoon** varianssin lähteitä:

-   Tuotantotilauksen hyväksytty määrä poikkeaa vakiokustannuslaskennassa käytetystä laskelman määrästä. Määrää käytetään vakiokustannusten kuoletuksen perustana.
-   Tuotantotilauksen vakiokustannusten arvo poikkeaa vakiokustannuslaskennassa käytetyistä vakiokustannuksista. Tuotantotilauksen vakiokustannukset voivat olla erilaisia monista eri syistä. Vakiokustannuksiin voivat vaikuttaa esimerkiksi seuraavat tekijät:
    -   Tuotannon tuoterakenteen (BOM) tai reitityksen manuaaliset muutokset
    -   Toisen tuoterakenneversion (BOM) tai reititysversion valinta tuotantotilausta luotaessa
    -   Suunnitellut muutokset nimikkeelle määritetyssä tuoterakenneversiossa tai reitityksessä.

Seuraavassa on joitakin tyypillisiä **tuotantohinnan** varianssin lähteitä:

-   Reititystoiminnon ilmoitetun kulutuksen kustannusluokka (ja kustannusluokan hinta) eroavat vakiokustannuslaskennassa käytettävästä kustannusluokasta.
-   Kustannusluokan hinnan aktiivinen kustannus eroaa vakiokustannuslaskennassa käytettävästä kustannusluokan hinnasta.

Seuraavassa on joitakin tyypillisiä **tuotantomäärän** varianssin lähteitä:

-   Materiaalikomponentteja otetaan varastosta liikaa tai liian vähän.
-   Reititystoiminnon raportointiaika on liian pitkä tai liian lyhyt.
-   Tilauksen määrään liittyvän päänimikkeen hyväksytty määrä ylitetään tai alitetaan. Kuitenkin tuotantotilauksen tilausmäärään perustuvat komponentit otetaan samalla varastosta kokonaan ja tuotantotilauksen tilausmäärään perustuvat toiminnot raportoidaan.

Seuraavassa on joitakin tyypillisiä **Tuotannon korvaus** varianssin lähteitä:

-   Varastosta otetaan materiaalikomponentti, jota ei ole tuotannon tuoterakenteessa.
-   Tuotannon tuoterakenteeseen lisätään komponentti ja raportoidaan se kulutetuksi manuaalisesti.
-   Raportoidaan nimike kulutetuksi, muttei lisätä sitä manuaalisesti tuotannon tuoterakenteeseen.
-   Tuotannon reititykseen lisätään toiminto, joka raportoidaan kulutetuksi manuaalisesti.
-   Valitaan eri tuoterakenneversio tuotantotilausta luotaessa, jolloin tuoterakenneversio eroaa vakiokustannuslaskennassa käytettävästä tuoterakenneversiosta.
-   Valitaan eri reititysversio tuotantotilausta luotaessa, jolloin reititysversio eroaa vakiokustannuslaskennassa käytettävästä reititysversiosta.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]