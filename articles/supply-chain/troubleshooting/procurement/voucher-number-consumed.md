---
title: Tuotteen vastaanoton tositenumero käytetään, vaikka tositetta ei luoda
description: Tuotteen vastaanoton tositenumero käytettään, vaikka tuotteen vastaanoton aikana ei luotaisi rahoitustositetta
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476222"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Tuotteen vastaanoton tositenumero käytetään, vaikka tositetta ei luoda

## <a name="symptoms"></a>Oireet

Tuotteen vastaanoton tositenumero käytettään, vaikka tuotteen vastaanoton aikana ei luotaisi rahoitustositetta.

## <a name="resolution"></a>Ratkaisu

Jos **Jaksota ostovelka tuotteen vastaanotossa** -asetuksen arvoksi on määritetty *Ei* nimikemalliryhmän osalta, kirjanpitoon ei tehdä kirjauksia. Fyysinen tapahtuma kirjataan kuitenkin kirjanpitotarkoituksia varten alikirjanpitoon, ja tapahtuma vaatii tositenumeron. Tämä tositenumero on se tositenumero, johon viitataan varastotapahtumissa.

On suositeltavaa määrittää **Jaksota ostovelka tuotteen vastaanotossa** -asetuksen arvoksi *Kyllä*, kuten seuraavassa blogikirjoituksessa kuvataan: [Muiden kulujen kirjaaminen tuotteen vastaanoton hetkellä](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
