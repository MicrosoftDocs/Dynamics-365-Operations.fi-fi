---
title: Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla
description: Tässä aiheessa kuvataan, miten laskurekisteriä käytetään laskujen luomiseen.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9c54f610e45d288ed58fd209d290d73bfe1ff2f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820662"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten laskurekisteriä käytetään laskujen luomiseen. Käytä sitten laskupoolia laskun ja ostotilauksen täsmäyttämisessä ja viimeistele kulu toimittajan laskun sivulla.


## <a name="create-a-purchase-order"></a>Ostotilauksen luominen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Ostotilaukset**.
2. Luo uusi ostotilaus valitsemalla **Uusi**.
3. Avaa avattava luettelo **Toimittajan tili** -kentässä valitaksesi toimittajan. Voit valita esimerkiksi toimittajan **1001**.
4. Valitse **OK**.
5. Valitse **Nimiketunnus**-kentässä avattavasta valikosta palvelun nimiketunnus. Voit valita esimerkiksi arvon **S0001**. Nettosumma on 75,00 euroa.  Tämä on laskuun odotettava summa.  
6. Valitse toimintoruudussa **Osto**.
7. Valitse **Vahvista**.

## <a name="create-and-post-and-invoice"></a>Luominen, kirjaaminen ja laskuttaminen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskurekisteri**.
2. Valitse **Uusi**.
3. Avaa haku, kun haluat valita käytettävän laskurekisterin nimen.
4. Valitse sen laskurekisterin nimi, jota haluat käyttää.
5. Valitse **Rivit**, kun haluat avata rekisterin ja syöttää kulurivejä.
6. Valitse toimittaja haun avulla. Voit valita esimerkiksi toimittajan **1001**.
7. Syötä **Lasku**-kenttään laskunumero.
8. Kirjoita **Kuvaus**-kenttään arvo.
9. Syötä **Kredit**-kenttään numero.
10. Avaa **Ostotilaus-** kentässä avattava luettelo, jossa voit valita aiemmin luomasi ostotilauksen.
11. Korosta **Hyväksynyt**- kentässä avattavassa luettelossa hyväksyjä ja valitse hyväksyjä valitsemalla **Valitse.**
12. Valitse **Kirjaa**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Laskutusprosessin tekeminen valmiiksi avaamalla lasku poolista ja täsmäyttämällä se ostotilauksen kanssa
1. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Laskut > Laskupooli**.
2. Luo toimittajan lasku poolissa olevasta laskusta valitsemalla **Ostotilaus**.
3. Valitse lasku, jota haluat tarkastella.
4. Tee täsmäytys valmiiksi valitsemalla **Päivitä täsmäytyksen tila**.
5. Valitse toimintoruudussa **Asetukset**.
6. Valitse **Vaihda näyttö**.
7. Valitse **Ruudukkonäkymä**.
8. Valitse **Kirjaa**.
9. Sulje lomake.
10. Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Toimittajat > Toimittajat**.
11. Valitse ostotilauksessa mainittu toimittaja. Voit valita esimerkiksi toimittajan **1001**.
12. Valitse toimintoruudussa **Toimittaja**.
13. Valitse **Tapahtumat**.
14. Valitse luomasi lasku. Laskurekisterin jaksotus peruutettiin ja kirjattiin sopivalle kulutilille.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]