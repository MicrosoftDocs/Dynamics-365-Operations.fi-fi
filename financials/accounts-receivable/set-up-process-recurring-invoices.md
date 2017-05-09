---
title: "Aseta ja käsittele toistuvia laskuja"
description: "Tässä artikkelissa kerrotaan, miten toistuvat laskut määritetään ja miten niitä käsitellään. Voit käyttää toistuvia laskuja, jos asiakkailta laskutetaan sama summa säännöllisesti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f14e9227ef56f428d18999aa7b52254580cdfa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-and-process-recurring-invoices"></a>Aseta ja käsittele toistuvia laskuja

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten toistuvat laskut määritetään ja miten niitä käsitellään. Voit käyttää toistuvia laskuja, jos asiakkailta laskutetaan sama summa säännöllisesti.

<a name="create-a-recurring-free-text-invoice-template"></a>Luo malli toistuville vapaatekstilaskuille
---------------------------------------------

Laskuttaaksesi samoja säännöllisin väliajoin palveluita käyttäviä asiakkaita, on määritettävä vapaa tekstimuotoinen laskutusmalli, jota voidaan käyttää uudelleen laskujen luomiseen. Tämä malli sisältää seuraavat tiedot:

-   Otsikkotiedot, kuten veroryhmät, maksuehdot ja maksutapa
-   Rivin tietoja, kuten palvelun kuvaus, tulostilit, yksikköhinta ja laskutussumma
-   Toimitus-tai käsittelymaksut
-   Kirjanpidolliset jaot sekä taloushallinnon dimension tiedot, kuten kustannuspaikat ja liiketoimintayksiköt

Itse asiassa luot koko laskun ja tallennat sen mallina. Voit määrittää mallit käyttämällä **toistuvat laskut** -sivuja.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Määritä vapaatekstilaskun malli asiakkaalle ja syötä toistuvat yksityiskohdat
Mallin luonnin jälkeen malli on määritettävä niille asiakkaille, joita haluat laskuttaa. Lisäksi, sinun on määritettävä milloin ja kuinka usein laskua käytetään. Voit määrittää malleja **lasku**-välilehdessä **asiakkaat**-sivulla. Lisää malli luetteloon ja päivitä seuraavat tiedot:

-   Alkamispäivämäärä ja halutessasi päättymispäivä toistuvaa laskutusta varten
-   Toistuvan laskutuksen käyttötiheys (esimerkiksi päivittäin tai kerran kuussa)
-   Laskutuksen enimmäissumma (jos tämä on pakollinen määritys)

Asiakkaalla voi olla useita malleja, joilla on eri maksutiheydet.

## <a name="generate-the-recurring-invoices"></a>Luo toistuvat laskut
**Toistuvat laskut **-sivulla on tehtävä, joka käsittelee toistuvien laskujen malleja. Määritä laskutuspäivämäärä ja malli laskujen luontia varten. Laskut luodaan ja jokaiselle käsiteltävälle laskutusryhmälle määritetään yksi toistuva tunnusnumero.
Kirjaa toistuvat vapaatekstilaskut
---------------------------------

Sen jälkeen kun toistuvat laskut on luotu, laskun toistuvat tunnukset näkyvät kirjaustehtävässä **toistuvat laskut **-sivulla. Voit tarkastella kaikkia laskuja toistuvalle tunnukselle napsauttamalla linkkiä. Voit poistaa yksittäisiä laskuja toituvan tunnuksen laskujen tarkistuksen aikana. Asiakkaan toistumisasetukset palautetaan kyseiseen malliin niin, että se voidaan ottaa esille myöhemmin uudelleen. Voit kirjata yhden, useita tai kaikki laskut toistuvalla tunnuksella. Jos työnkulkuja on otettu käyttöön, sinun on valittava **lähetä** ennen kuin voit kirjata laskut.
Tulosta toistuvat vapaatekstilaskut
----------------------------------

Sen jälkeen kun toistuvat laskut on kirjattu, voit tulostaa laskuja vapaan tekstimuotoisen laskun luettelosivulta. Voit tulostaa laskut, jotka on valittu tai voit valita mitkä laskut haluat tulostaa.




