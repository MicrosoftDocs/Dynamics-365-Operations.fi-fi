---
title: Työtilauspoolit
description: Tässä ohjeaiheessa kerrotaan työtilauspoolien käsittelystä resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875631"
---
# <a name="work-order-pools"></a>Työtilauspoolit


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Voit käyttää työtilauspooleja sellaisten työtilausten ryhmittelyyn, joilla on jotain yhteistä. Voit esimerkiksi luoda työtilauspooleja seuraavasti:

- työnjoukkueille, esimerkiksi huoltomiehistö A, huoltomiehistö B  

- osaamisille, esimerkiksi sähköasentajat tai putkimiehet  

- fyysinen sijainti  

- aikatauluille, esimerkiksi viikot tai muut kaudet  


Jos tarpeen, yksi työtilaus voidaan sijoittaa moniin työtilauspooleihin.


## <a name="create-work-order-pool"></a>Luo työtilauspooli

**Kaikki työtilauspoolit**- tai **Aktiiviset työtilauspoolit**- kodissa saat yleiskuvan työtilauspooleista ja voit luoda uusia pooleja.

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **Työtilauspoolit** >  **Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit**.

2. Valitse **Uusi**.

3. Lisää työtilauspoolin tunnus **pooli**-kenttään ja nimi **Nimi**-kenttään.

4. Valitse "kyllä" **Aktiivinen**-vaihtopainikkeen avulla osoittamaan, että työtilauspooli on aktiivinen.

5. Valitse **Poista työtilauksen suhteet** -vaihtopainikkeessa "kyllä", jos haluat, että työtilaukset poistetaan automaattisesti työtilauspoolista.

6. Valitse **Poista elinkaaren tila** -kentässä työtilauksen elinkaaritila. Esimerkiksi työtilauksen suorittamisen elinkaaritila voidaan määrittää poistamaan automaattisesti suhteet työtilauspooleihin.

7. Voit aloittaa työtilausten lisäämisen työtilauspooliin heti. Valitse **Työtilaukset** -pikavälilehdessä **Lisää rivi**.

8. Valitse **Työtilaus**-kentässä työtilaus. Liittyvät kentät päivittyvät automaattisesti.

9. Toista vaiheet 7-8, jos haluat lisätä uusia työtilauksia.

10. **Lajittelujärjestys**-kentässä voit määrittää, suoritetaanko työtilaukset tietyssä järjestyksessä. Voit määrittää valittujen työtilausten tietyn järjestyksen lisäämällä luvut 1, 2, 3 ja niin edelleen.

11. Napsauttamalla **Työtilaukset**-painiketta saat näkyviin luettelon kaikista työtilauspooliin sisältyvistä työtilauksista.

12. Valitsemalla **kapasiteetin kuormitus** -painikkeen voit avata **Kapasiteetin kuormitus** -kohdan, joka laskee ja näyttää ylläpitoaikataulun, ei-ajoitettujen työtilausten ja ajoitettujen työtilausten kapasiteetin kuormituksen.

13. Valitse **Nimike-ennuste**-painike, kun avata **Nimike-ennusteen** laskeaksesi ja tarkastellaksesi nimikkeiden (varaosien ja muiden tarvittavien nimikkeiden) ennusteita, jotka liittyvät kunnossapitoaikatauluun, ei-ajoitettuihin työtilauksiin ja ajoitettuihin työtilauksiin.

14. Avaa **Työtilauksen ostoehdotus** -luettelo napsauttamalla **Työtilauksen ostoehdotus** -painiketta, niin saat näkyviin luettelon työtilauspoolin työtilauksiin liittyvistä ostoehdotuksista.

15. Avaa **Työtilauksen osto** -luettelo napsauttamalla **Työtilauksen osto** -painiketta, niin saat näkyviin luettelon työtilauspoolin työtilauksiin liittyvistä ostotilauksista.

>[!NOTE]
>Kun työtilauspooli ei ole enää tarpeen työsuunnitelmasi osalta, määritä kyseisen varannon **Aktiivinen**-valintaruutuun Ei **Työtilauspooli**-luettelonäkymässä.

Valitse **Poista työtilaussuhteet** -valintaruutu, jos haluat poistaa kaikki työtilausrivit, esimerkiksi luodaksesi tyhjän varannon, jota voit myöhemmin käyttää muissa työtilauksissa. Muista tyhjentää **Poista työtilauksen suhteet** -valintaruutu, jos haluat käyttää työtilauspoolia uusien työtilaussuhteiden luomiseen myöhemmin.


![Kuva 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Työtilauksen lisääminen työtilauspooliin

Kuten yllä olevassa osassa on kuvattu, voit lisätä työtilauksia työtilauspooliin, kun luot poolin. Voit myös lisätä työtilauksen työtilauspooliin jostakin **Kaikki työtilaukset** -luettelosta.

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus luettelosta ja valitse sitten **Työtilauspooli.**

3. Valitse **Lisää/poista** -kentässä Lisää.

4. Valitse työtilauspooli **Pooli**-kentässä.

5. Valitse **OK**.

6. Kun olet lisännyt työtilauksen työtilauspooliin ja haluat sijoittaa työtilauksen poolin tiettyyn kohtaan: Avaa jokin työtilauspooli luettelosivulta, valitse pooli ja valitse **Muokkaa**ja säädä poolin työtilausten lajittelujärjestystä kohdassa **Työtilauspooli** -lomake > > **Työtilaukset**- pikavälilehti > **Lajittelujärjestys**-kenttä.

Jos haluat poistaa valitun työtilauksen työtilauspoolista, valitse Poista vaiheessa 3.

