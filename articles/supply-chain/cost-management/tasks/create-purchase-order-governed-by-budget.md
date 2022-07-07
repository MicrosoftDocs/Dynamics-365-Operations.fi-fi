---
title: Ostotilauksen luonti budjetin mukaan
description: Tämän menettelyn avulla voit luoda ostotilauksen, jonka käytettävissä oleva budjetti tarkistetaan.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016185"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Ostotilauksen luonti budjetin mukaan

[!include [banner](../../includes/banner.md)]

Tämän menettelyn avulla voit luoda ostotilauksen, jonka käytettävissä oleva budjetti tarkistetaan.

## <a name="review-the-budget-control-configuration"></a>Budjetin hallinnan konfiguraation tarkistaminen

1. Valitse **Budjetointi > Asetukset > Budjetin hallinta > Budjetin hallinnan konfiguraatio**.
1. Valitse **Käytettävissä olevat budjettivarat** -välilehti.
1. Valitse **Tiedostot ja kirjauskansiot** -välilehti.
1. Valitse **Määritä budjetin hallintasäännöt** -välilehti.
1. Valitse **Määritä budjettiryhmät** -välilehti.
1. Sulje sivu.

## <a name="create-a-purchase-order"></a>Luo ostotilaus

1. Valitse **Hankinta > Ostotilaukset > Kaikki ostotilaukset**.
1. Valitse **Uusi**.
1. Anna tai valitse arvo **Toimittajatili**-kentässä.
1. Laajenna **Yleinen**-pikavälilehti.
1. Määritä **Kirjauspäivä**-kenttään päivämäärä.
1. Valitse **OK**, jos haluat sulkea valintaikkunan ja avata uuden ostotilauksen.
1. Valitse **Ostotilausrivit**-pikavälilehden työkalurivillä **Lisää rivi** ja lisää uusi rivi. Lisää nimike tilaukseen täyttämällä rivi vaaditulla tavalla.
1. Valitse **Ostotilausrivi**-pikavälilehden työkalurivillä **Myyntitiedot \> Jaa summat**.
1. Määritä **Kirjanpitotili**-kenttään summa.
1. Sulje sivu.

## <a name="perform-budget-checking"></a>Tarkista budjetti

1. Jatka sen ostotilauksen käsittelyä, johon rivi lisättiin.
1. Valitse **Ostotilausrivi**-pikavälilehden työkalurivillä **Myyntitiedot \> Tarkista budjetti**.
1. Valitse **Ostotilausrivi**-pikavälilehden työkalurivillä **Myyntitiedot \> Budjetin tarkistuksen virheet ja varoitukset**.
1. **Budjetin tarkistuksen virheet ja varoitukset** -valintaikkuna avautuu. Tarkista tarkistuksen tulokset ja sulje valintaikkuna valitsemalla **Sulje**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]