---
title: Rahdin täsmäytys kuljetustenhallinnassa
description: Tässä aiheessa käsitellään rahdin täsmäytysprosessia.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e1680572f1ba9816c9ec45ef52498cab1f45247
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206216"
---
# <a name="reconcile-freight-in-transportation-management"></a>Rahdin täsmäytys kuljetustenhallinnassa

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään rahdin täsmäytysprosessia.

Rahti voidaan täsmäyttää manuaalisesti tai se voidaan määrittää tapahtumaan automaattisesti. Jos haluat käyttää rahdin automaattista täsmäytystä, sinun on määritettävä päätarkistus, jossa voit määrittää ehdot määrittämään automaattisesti täsmäytettävät rahtilaskut.

## <a name="the-freight-reconciliation-process"></a>Rahdin täsmäytysprosessi
Kuljetusmaksut lasketaan hinnan laskennassa, joka on liitetty soveltuvaan rahdinkuljettajaan. Kun kuorma on vahvistettu, rahtilasku luodaan ja rahtitaksat siirretään siihen. Rahtitaksat jaetaan sekalaisina kuluina soveltuvaan lähdeasiakirjaan (ostotilaus, myyntitilaus ja/tai siirtotilaus) sen mukaan, mitä asetuksia tavallisen laskutusprosessin asetuksissa on käytetty. Rahdin täsmäytysprosessi voi alkaa heti, kun rahdinkuljettajan rahtilasku saadaan. Kyse voi olla sähköisestä laskusta tai paperilaskusta. Jos kyse on paperilaskusta, voit luoda sähköisen laskun käyttämällä rahtilaskua mallina. 

[![Rahdin täsmäytysprosessi](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuaalinen täsmäytys
Jos olet täsmäyttämässä rahtia manuaalisesti, sinun on täsmäytettävä kukin laskun rivi rahtilaskun rivin tai laskutettavan kuorman rivien kanssa. Tämä täsmäytys tehdään **Rahtilaskun ja laskun täsmäytys** -sivulla. Jos laskurivin summa ei täsmää rahtilaskun summan kanssa, valitse erolle täsmäytyssyy. Jos täsmäytyksellä on useita syitä, voit jakaa täsmäyttämättömät summan niiden kesken. Täsmäytyksen syy määrittää, miten eriävät summat kirjataan kirjanpitoon. Kun koko laskutussumma on täsmäytetty, se lähetetään hyväksytyksi, jonka jälkeen kirjauskansio kirjataan. Seuraavassa kuvassa on esitetty, kuinka voit luoda rahtilaskun ja suorittaa rahdin täsmäytyksen. 
[![Rahdin täsmäytystehtävät](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automaattinen täsmäytys
Jos haluat käyttää automaattista täsmäytystä, sinun on määritettävä täsmäytysaikataulu ja käytettävät laskut ja rahdinkuljettajat. Laskurivit ja rahtilaskut täsmäytetään päätarkistuksen ja rahtilaskun tyypin asetusten mukaan. Kun olet suorittanut automaattisen täsmäytyksen, sinun on käsiteltävä kaikki laskut, joita järjestelmä ei voi täsmäyttää. Nämä laskut on sitten käsiteltävä manuaalisesti ennen kaikkien laskujen kirjaamista maksettaviksi.



