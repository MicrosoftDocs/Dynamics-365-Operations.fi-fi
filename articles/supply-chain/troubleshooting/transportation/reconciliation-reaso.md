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
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750879"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Täsmäytysssyistä voit lisätä vain päätilin kredit-tiliksi

Tietopankin numero: 4603538

## <a name="symptoms"></a>Oireet

Kun määrität täsmäytyksen syyn kuljetuksen hallinnassa, voit lisätä vain päätilin kredit-tiliksi. Kustannuspaikkaa tai muuta dimensiota ei voi lisätä kredit-tiliksi. Debet-tilin avulla voit kuitenkin valita muita dimensioita.

## <a name="resolution"></a>Ratkaisu

Jos täsmäytystä ei ole tehty toimittajalle maksamiseksi vaan tietyn päätilin hyvittämiseksi, järjestelmä ei salli taloushallinnon dimension valitsemista kredit-tilille täsmäytyksen syytä määrittäessäsi.

Jos tilirakenne edellyttää tiettyä taloushallinnon dimension arvoa kredit-päätilille, tuloksena syntyvää toimittajakirjauskansiota ei voi kirjata automaattisesti, koska taloushallinnon dimension arvo puuttuu. Siksi hyvitystili on määritettävä manuaalisesti **Laskukirjauskansio**-sivulla.

Koska kredit-tilille tarvitaan dimensioarvo, toimittajan laskukirjauskansiota ei voi kirjata automaattisesti. Se on kirjattava manuaalisesti sen jälkeen, kun dimensioarvo on lisätty hyvitysrivin päätilille manuaalisesti.
