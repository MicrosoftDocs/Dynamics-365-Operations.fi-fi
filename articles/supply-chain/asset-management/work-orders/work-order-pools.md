---
title: Työtilauspoolit
description: Tässä ohjeaiheessa kerrotaan työtilauspoolien käsittelystä resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dd474451569e123fab811cc3625862d599a07963f3714c72d5a724ffd052983e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733513"
---
# <a name="work-order-pools"></a>Työtilauspoolit

[!include [banner](../../includes/banner.md)]


Voit käyttää työtilauspooleja sellaisten työtilausten ryhmittelyyn, joilla on jotain yhteistä. Tässä on esimerkkejä asioista, joita varten voit luoda työtilauspooleja:

- Työvuorot, kuten Ylläpitovuoro A tai Ylläpitovuoro B  

- Osaaminen, kuten sähköasentajat tai putkimiehet  

- Fyysiset sijainnit  

- Aikataulut, kuten viikot tai muut ajanjaksot  

Tarvittaessa voit laittaa yhden työtilauksen useaan työtilauspooliin.


## <a name="create-a-work-order-pool"></a>Työtilauspoolin luominen

Luettelosivulla **Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit** saat yleiskuvan työtilauspooleista ja voit luoda uusia pooleja.

1. Valitse **Resurssien hallinta** > **yhteiset** > **Työtilauspoolit** > **Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit**.

2. Valitse **Uusi**.

3. Kirjoita **Pooli**-kenttään työtilauspoolin tunnus.

4. Anna nimi **Nimi**-kenttään.

5. Aseta **Aktiivinen**-asetuksen arvoksi **Kyllä** ilmaisemaan, että työtilauspooli on aktiivinen.

6. Aseta **Poista työtilauksen suhteet** -asetuksen arvoksi **Kyllä**, jos työtilaukset on tarkoitus poistaa automaattisesti työtilauspoolista.

7. Valitse **Poista elinkaaren tila** -kentässä työtilauksen elinkaaritila. Esimerkiksi työtilauksen suorittamisen elinkaaritila voidaan määrittää poistamaan automaattisesti suhteet työtilauspooleihin.

    Voit aloittaa työtilausten lisäämisen työtilauspooliin heti.

8. Valitse **Työtilaukset** -pikavälilehdessä **Lisää rivi**.

9. Valitse **Työtilaus**-kentässä työtilaus. Liittyvät kentät päivittyvät automaattisesti.

10. Voit lisätä muita työtilauksia tekemällä kohtien 8–9 toimet uudelleen.

11. Jos lisäämäsi työtilaukset on tarkoitus suorittaa tietyssä järjestyksessä, voit määrittää järjestyksen syöttämällä **Lajittelujärjestys**-kenttään numerot **1**, **2**, **3** jne.

12. Voit tarkastella luetteloa kaikista työtilauspooliin kuuluvista työtilauksista valitsemalla **Työtilaukset** toimintoruudun **Työtilauspooli**-välilehden **Näytä työtilauspooliin liittyvät** -ryhmässä, jolloin **Kaikki työtilaukset** -luettelosivu avautuu.

13. Voit laskea ylläpitoaikataulun, ajoittamattomien työtilausten ja ajoitettujen työtilausten kapasiteetin kuormituksen ja tarkastella sitä valitsemalla **Kapasiteetin kuormitus** toimintoruudun **Työtilauspooli**-välilehden **Näytä työtilauspooliin liittyvät** -ryhmässä, jolloin avautuu **Laske kapasiteetin kuormitus** -valintaikkuna.

14. Voit laskea ylläpitoaikatauluun, ajoittamattomiin työtilauksiin ja ajoitettuihin työtilauksiin liittyvien nimikkeiden (varaosien ja muiden tarvittavien nimikkeiden) ennusteita ja tarkastella niitä valitsemalla **Nimike-ennuste** **Työtilauspooli**-välilehden **Näytä työtilauspooliin liittyvät** -ryhmässä, jolloin avautuu **Laske nimike-ennuste** -valintaikkuna.

15. Voit tarkastella työtilauspoolin työtilauksiin liittyvien ostoehdotusten luetteloa valitsemalla **Työtilauksen ostoehdotus** toimintoruudun **Työtilauspooli**-välilehden **Hankinta**-ryhmässä, jolloin **Työtilauksen ostoehdotus** -luettelosivu avautuu.

16. Voit tarkastella työtilauspoolin työtilauksiin liittyvien ostotilausten luetteloa valitsemalla **Työtilauksen osto** toimintoruudun **Työtilauspooli**-välilehden **Hankinta**-ryhmässä, jolloin **Työtilauksen osto** -luettelosivu avautuu.

>[!NOTE]
>Kun työtilauspooli ei ole enää tarpeen työsuunnitelmasi osalta, määritä kyseisen poolin **Aktiivinen**-asetuksen arvoksi **Ei** **Työtilauspooli**-sivun luettelonäkymässä.

Voit poistaa kaikki työtilausrivit asettamalla **Poista työtilaussuhteet**-asetuksen arvoksi **Kyllä**. Tämä asetus on hyödyllinen, jos esimerkiksi haluat luoda tyhjän poolin, jota voit käyttää myöhemmin muita työtilauksia varten. Kun myöhemmin olet valmis käyttämään työtilauspoolia uusien työtilaussuhteiden luomiseen, muista asettaa **Poista työtilaussuhteet** -asetuksen arvoksi **Ei**.

Seuraavassa kuvassa on esimerkki **Työtilauspooli** -luettelosivusta.

![Kuva 1.](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Työtilauksen lisääminen työtilauspooliin

Kuten edellisessä osassa on kuvattu, voit lisätä työtilauksia työtilauspooliin, kun luot poolin. Voit myös lisätä työtilauksia työtilauspooliin luettelosivulla **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

1. Valitse työtilaus luettelosta ja sitten toimintoruudun **Työtilaus**-välilehden **Ylläpidä**-ryhmässä **Työtilauspooli**.

2. Valitse työtilaus luettelosta ja valitse sitten **Työtilauspooli.**

3. Valitse **Ylläpidä työtilauspoolia** -valintaikkunan **Lisää/poista**-kentässä **Lisää**.

4. Valitse työtilauspooli **Pooli**-kentässä.

5. Valitse **OK**.

6. Jos haluat asettaa lisäämäsi työtilaukset tiettyyn järjestykseen työtilauspoolissa, valitse pooli luettelosivulla **Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit** ja valitse **Muokkaa**. Käytä sitten **Työtilauspooli**-sivun **Työtilaukset**-pikavälilehden **Lajittelujärjestys**-kenttää muuttaaksesi pooliin kuuluvien työtilausten lajittelujärjestystä.

Voit poistaa työtilauksen työtilauspoolista toistamalla nämä vaiheet, mutta valitsemalla **Poista** vaiheessa 3.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]