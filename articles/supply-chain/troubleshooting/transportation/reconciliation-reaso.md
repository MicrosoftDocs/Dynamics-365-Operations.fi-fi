---
title: Täsmäytysssyistä voit lisätä vain päätilin kredit-tiliksi
description: Kun määrität täsmäytyksen syyn kuljetuksen hallinnassa, voit lisätä vain päätilin kredit-tiliksi.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026459"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Täsmäytysssyistä voit lisätä vain päätilin kredit-tiliksi

Tietopankin numero: 4603538

## <a name="symptoms"></a>Oireet

Kun määrität täsmäytyksen syyn kuljetuksen hallinnassa, voit lisätä vain päätilin kredit-tiliksi. Kustannuspaikkaa tai muuta dimensiota ei voi lisätä kredit-tiliksi. Debet-tilin avulla voit kuitenkin valita muita dimensioita.

## <a name="resolution"></a>Ratkaisu

Jos täsmäytystä ei ole tehty toimittajalle maksamiseksi vaan tietyn päätilin hyvittämiseksi, järjestelmä ei salli taloushallinnon dimension valitsemista kredit-tilille täsmäytyksen syytä määrittäessäsi.

Jos tilirakenne edellyttää tiettyä taloushallinnon dimension arvoa kredit-päätilille, tuloksena syntyvää toimittajakirjauskansiota ei voi kirjata automaattisesti, koska taloushallinnon dimension arvo puuttuu. Siksi hyvitystili on määritettävä manuaalisesti **Laskukirjauskansio**-sivulla.

Koska kredit-tilille tarvitaan dimensioarvo, toimittajan laskukirjauskansiota ei voi kirjata automaattisesti. Se on kirjattava manuaalisesti sen jälkeen, kun dimensioarvo on lisätty hyvitysrivin päätilille manuaalisesti.
