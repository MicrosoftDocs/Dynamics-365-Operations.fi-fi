---
title: Varmennepolun virhe päivitettäessä tai siirryttäessä WMS:ään
description: Jos sovelluksessa näkyy virhe "Varmennepolun luottamusankkuria ei löydy", kun päivitetään tai siirrytään WMS:ään, tämä sivu sisältää tiedot ongelman ratkaisemiseen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476202"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Varmennepolun luottamusankkuria ei löydy päivityksen ja WMS:ään siirtymisen aikana

## <a name="symptoms"></a>Oireet

Päivitettäessä ja siirryttäessä edistyneeseen varastonhallintaan (WMS), Warehouse Management -sovellus saattaa antaa seuraavan virhesanoman:

> java.security.cert.certPathValidatorException: Varmennepolun luottamusankkuria ei löydy.

## <a name="cause"></a>Syy

Tämä johtuu siitä, että Android 8+ ei luota itse allekirjoitettuihin varmenteisiin paikallisissa ympäristöissä.

## <a name="resolution"></a>Ratkaisu

Käytä ulkoista (julkista) varmenteiden myöntäjää. Tämän Warehouse Management -sovelluksen ongelman korjaus on saatavana versiossa 1.9.0.0. Lisätietoja tästä ongelmasta ja sen korjaamisesta: [Varmennepolun luottamusankkuria ei löydy määritettäessä sovellusyhteyttä](certification-path-app-connection-error.md)
