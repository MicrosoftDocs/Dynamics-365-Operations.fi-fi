---
title: Luo ostosopimus
description: Tämä ohjeaihe opastaa luomaan ostosopimuksen.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92c9b429a05a2c25672cc14a0c9ee7adfef42631
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016828"
---
# <a name="create-a-purchase-agreement"></a>Luo ostosopimus

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe opastaa luomaan ostosopimuksen. Se on yleensä ostopäällikön tehtävä. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi. Ennen aloittamista on määritettävä ostosopimusluokitukset. Kun olet luonut sopimuksen, voit luoda sen avulla ostotilauksen, jolloin ostotilauksen ehdot kopioituvat otsikkoon ja niille tilauksen riveille, joihin sopimus vaikuttaa.


## <a name="create-a-new-purchase-agreement"></a>Luo uusi ostosopimus
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostosopimukset > Ostosopimukset**.
2. Valitse **Uusi**.
3. Valitse uuden rivin **Toimittajan tili**-kentästä haluamasi tietue avattavasta valikosta.
4. Valitse uuden rivin **Ostosopimuksen luokitus**-kentästä haluamasi tietue avattavasta valikosta.
5. Laajenna **Yleinen**-pikavälilehti.
6. Kirjoita päivämäärä **Vanhentumispäivä**-kenttään.

    - Tämä vanhentumispäivä on kaikkien sitoutumisrivien oletusarvo ja määrittää, miten kauan kukin sitoutuminen on voimassa.  

7. Kirjoita **Asiakirjan nimi** -kenttään ostosopimuksen nimi.

    - Jätä **Oletussitoumus** -kentän arvoksi **Tuotteen määrän vahvistus** (tai vaihda tarvittaessa tähän arvoon).  
    - Sitoutumisen oletusavo määrittää sopimusrivien vaihtoehdot. Jos tarvitset sopimuksen rivejä luodessasi uuden sitoutumistyypin, sinun on muutettava otsikon oletussitoutumista. Sitoutumistyyppejä on 4: **Tuotteen määrän vahvistus** – koskee tiettyä tuotemäärää. **Tuotteen arvon vahvistus** – koskee tuotteen tiettyä valuuttasumma. **Tuoteluokan arvon sitoutuminen** – koskee tiettyä hankintaluokan valuuttasummaa, jossa summa voi olla luettelonimike tai ei-luettelonimike. **Arvon sitoutuminen** – koskee tiettyä valuuttasumma, jonka voi täyttää mikä tahansa tuote tai hankintaluokka.  

8. Valitse **OK**.

## <a name="add-a-commitment"></a>Lisää sitoutuminen
1. Valitse **Lisää rivi**.
2. Valitse **Nimiketunnus**-kentässä avattavasta valikosta haluttu tietue.
3. Anna **Määrä**-kentässä numero. Kokonaismäärä, jonka olet sopinut ostavasi toimittajalta.  
4. Syötä **Yksikköhinta**-kenttään numero.
5. Laajenna **Rivin erittely** -osa.
6. Valitse **Maksimi pakotetaan** -asetukseksi **Kyllä**. **Maksimi pakotetaan** -vaihtoehto rajoittaa sitoutumisen käyttöä. Voit ostaa enintään rivin **Määrä**-kentässä määritetyn määrän.  

## <a name="add-header-conditions"></a>Lisää otsikkoehdot
1. Valitse toimintoruudussa **Asetukset**.
2. Valitse **Vaihda näyttö**.
3. Valitse **Otsikkonäkymä**.
4. Laajenna **Ehdot**-osa.
5. Valitse **Maksutapa**-kentässä avattavasta valikosta haluamasi tietue. Toimittajatilin maksuehdot näkyvät tässä oletusarvoisesti.  
6. Valitse **Toimitustapa**-kentässä avattavasta valikosta haluamasi tietue.
7. Avaa haku napsauttamalla **Toimitusehdot**-kentässä avattavan valikon painiketta.

## <a name="confirm-and-activate-the-agreement"></a>Vahvista ja aktivoi sopimus
1. Valitse toimintoruudussa **Ostosopimus**.
2. Valitse **Vahvistus**. Valitse **Merkitse sopimus voimassa olevaksi** -asetukseksi **Kyllä**.  
3. Valitse **OK**.
4. Valitse toimintoruudussa **Ostosopimus**.
5. Valitse **Ostosopimuksen vahvistukset**. **Esikatselu/tulostus**-vaihtoehdolla voi luoda ostosopimusasiakirjan, jonka voi tulostaa tai lähettää asiakkaalle. Jos päivität sopimusta myöhemmin ja vahvistat sen uudelleen, molemmat versiot näkyvät tässä.  
6. Sulje sivu.

