---
title: Määritä maksun toistuvuus
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5fe0a16c4abbb9241fcdac88fd56e92bf04788c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008941"
---
# <a name="set-up-payment-frequencies"></a>Määritä maksun toistuvuus

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources käyttää maksun toistuvuuksia vuosittaisen etuuspalkan laskemiseen, määrittää etuuspalkan summan, jonka työntekijä maksaa kullekin maksukaudelle, ja määrittää, kuinka usein maksut tehdään palveluntarjoajille.

Etujen maksutiheydet käyttävät muuntokertoimia, joilla muunnetaan etumaksuja kuukausittaisten, puolikuukausittaisten, kahden viikon välein tapahtuvien ja päivittäisten maksutaajuuksien välillä. Tämän avulla yritykset voivat määrittää Etusuunnitelman maksutiheyksien keskinäisen riippuvuuden.

Muuntokertoimet-kentät määrittävät muuntokertoimen maksutaajuuksista vakiomaksukausille ja sallivat järjestelmän tehdä laskutoimituksia maksutaajuuksien välillä. Muuntokerroin määrää käytetään myös määritettäessä etupalkkiosumma, joka työntekijän tulisi maksaa jokaisella maksutiheydellä.

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Maksun taajuudet**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | Maksun toistuvuus | Yksilöivä maksutaajuuksien nimi. |
   | Kuvaus | Maksutiheyden kuvaus. |
   | Kausi | Sopiva kausi, joka parhaiten vastaa edun tarjoajan ja työntekijän maksutiheyttä. Kausiluettelo koostuu vakiomaksuista. |
   | Maksukausien määrä | Maksukausien määrä, joka ilmaisee, kuinka usein edun toimittajalle tai työntekijöille maksetaan. Tätä määrää käytetään laskettaessa työntekijän vuosittaisen etuuden palkkasumma. |
   | Vuosittainen muuntokerroin | Toimitustiheyden vuosittainen muuntokerroin. Esimerkiksi kuukausittaisen maksutiheyden vuosittainen muuntokerroin on seuraava: </br></br>(12 kuukausimaksua/1 vuosi) = 12 |
   | Puolivuosittainen muuntokerroin | Toimitustiheyden puolivuosittainen muuntokerroin. Esimerkiksi kuukausittaisen maksutiheyden puolivuosittainen muuntokerroin on seuraava: </br></br>(12 kuukausimaksua/2 kertaa vuodessa) = 6 |
   | Neljännesvuosittainen muuntokerroin | Toimitustiheyden neljännesvuosittainen muuntokerroin. Esimerkiksi kuukausittaisen maksutiheyden neljännesvuosittainen muuntokerroin on seuraava: </br></br>(12 kuukausimaksua/4 neljäsosaa) = 3 |
   | Kuukausittainen muuntokerroin | Toimitustiheyden kuukausittainen muuntokerroin. Esimerkiksi kuukausittaisen maksutiheyden kuukausittainen muuntokerroin on seuraava: </br></br>(12 kuukausimaksua/12 kuukautta) = 1 |
   | Puolikuukausittainen muuntokerroin | Kaksi kertaa kuukaudessa tapahtuvan toimitustiheyden muuntokerroin. Esimerkiksi kaksi kertaa kuukaudessa tapahtuvan maksutiheyden kuukausittainen muuntokerroin on seuraava: </br></br>(12 kuukausittaista maksua/24 (2 x kuukaudessa)) = 0,5 | 
   | Puoliviikoittainen muuntokerroin | Toimitustiheyden vuosittainen muuntokerroin. Esimerkiksi kuukausittaisen maksutiheyden vuosittainen muuntokerroin on seuraava: </br></br>(12 kuukausimaksua/26 viikkoa) = 0,461538 |
   | Viikoittainen muuntokerroin | Toimitustiheyden vuosittainen muuntokerroin. Esimerkiksi kuukausittaisen maksutiheyden vuosittainen muuntokerroin on seuraava: </br></br>(12 kuukausimaksua/52 viikkoa) = 0,230769 |
   | Päivittäinen muuntokerroin | Toimitustiheyden vuosittainen muuntokerroin. Esimerkiksi kuukausittaisen maksutiheyden vuosittainen muuntokerroin on seuraava: </br></br>(12 kuukausimaksua/365 päivää) = 0,032877 |

4. Valitse **Tallenna**. 
