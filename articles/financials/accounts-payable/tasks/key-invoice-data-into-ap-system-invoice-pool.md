--- 
title: "Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla"
description: "Tässä tehtävän ohjauksessa kerrotaan, miten laskurekisteriä käytetään laskujen luomiseen."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävän ohjauksessa kerrotaan, miten laskurekisteriä käytetään laskujen luomiseen.  Käytä sitten laskupoolia laskun ja ostotilauksen täsmäyttämisessä ja viimeistele kulu toimittajan laskun sivulla.


## <a name="create-a-purchase-order"></a>Luo ostotilaus
1. Valitse Ostoreskontra > Ostotilaukset > Ostotilaukset.
2. Luo ostotilaus valitsemalla Uusi.
3. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
4. Valitse toimittaja luettelosta. Voit valita esimerkiksi toimittajan 1001.
5. Valitse OK.
6. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
7. Etsi luettelosta palveluiden nimiketunnus. Voit valita esimerkiksi arvon S0001.
8. Napsauta nimiketunnusta ja valitse se.
    * Nettosumma on 75,00 euroa.  Tämä on laskuun odotettava summa.  
9. Valitse toimintoruudussa Osto.
10. Valitse Vahvista.

## <a name="create-and-post-and-invoice"></a>Luominen, kirjaaminen ja laskuttaminen
1. Siirry kohtaan Ostoreskontra > Laskut > Laskurekisteri.
2. Valitse Uusi.
3. Avaa haku, kun haluat valita käytettävän laskurekisterin nimen.
4. Valitse sen laskurekisterin nimi, jota haluat käyttää.
5. Valitse Rivit, kun haluat avata rekisterin ja syöttää kulurivejä.
6. Valitse toimittaja haun avulla. Valitse esimerkiksi toimittaja 1001.
7. Syötä Lasku-kenttään laskunumero.
8. Kirjoita Kuvaus-kenttään arvo.
9. Syötä Kredit-kenttään numero.
10. Avaa haku valitsemalla Ostotilaus-kentässä avattavan valikon painike.
11. Valitse aiemmin luomasi ostotilaus.
12. Avaa haku valitsemalla Hyväksynyt-kentässä avattavan valikon painike.
13. Korosta hyväksyjä ja valitse hyväksyjä valitsemalla Valitse.
14. Valitse Kirjaa.
15. Sulje lomake.
16. Sulje lomake.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Laskutusprosessin tekeminen valmiiksi avaamalla lasku poolista ja täsmäyttämällä se ostotilauksen kanssa
1. Siirry kohtaan Ostoreskontra > Laskut > Laskupooli.
2. Luo toimittajan lasku poolissa olevasta laskusta valitsemalla Ostotilaus.
3. Valitse lasku, jota haluat tarkastella.
4. Tee täsmäytys valmiiksi valitsemalla Päivitä täsmäytyksen tila.
5. Valitse toimintoruudussa Asetukset.
6. Valitse Vaihda näkymä.
7. Valitse Ruudukkonäkymä.
8. Valitse Kirjaa.
9. Sulje lomake.
10. Valitse Ostoreskontra > Toimittajat > Toimittajat.
11. Valitse ostotilauksessa mainittu toimittaja. Voit valita esimerkiksi toimittajan 1001.
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Valitse toimintoruudussa Toimittaja.
14. Valitse Tapahtumat.
15. Valitse luomasi lasku.
    * Laskurekisterin jaksotus peruutettiin ja kirjattiin sopivalle kulutilille.  


