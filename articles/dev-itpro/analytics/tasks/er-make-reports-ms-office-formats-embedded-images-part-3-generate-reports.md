--- 
title: "Upotettuja kuvia sisältävien Microsoft Office -muotoisten raporttien luominen"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella sähköisen raportoinnin (ER) konfiguraatioita luomaan sähköisiä, upotettuja kuvia sisältäviä asiakirjoja MS Office -muodoissa (Excel ja Word)."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e2ab89857f4bf4844123508837c8faa504bc8839
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="generate-reports-in-microsoft-office-formats-with-embedded-images"></a>Upotettuja kuvia sisältävien Microsoft Office -muotoisten raporttien luominen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella sähköisen raportoinnin (ER) konfiguraatioita luomaan sähköisiä, upotettuja kuvia sisältäviä asiakirjoja MS Office -muodoissa (Excel ja Word).

Tässä esimerkissä luodaan ER-konfiguraatioita malliyritykselle Litware, Inc.  Voit suorittaa nämä vaiheet, kun suoritat ensin ER Upotettuja kuvia sisältävien raporttien tekeminen MS Office -muodoissa (Osa 2 – konfiguraatioiden tarkistaminen) -tehtäväoppaan vaiheet. Nämä vaiheet voidaan suorittaa USMF-yrityksessä.


## <a name="run-format-with-initial-model-mapping"></a>Muodon suorittaminen alkuperäisen mallin yhdistämismäärityksen kanssa
1. Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.
2. Pikasuodattimen avulla voit suodattaa Pankkitili-kentän USMF OPER -arvon mukaan.
3. Valitse toimintoruudussa Määritä.
4. Valitse Tarkista.
5. Valitse Tulosta testi.
    * Suorita muoto testausta varten.  
6. Valitse Siirtokelpoisen sekin muoto -kentässä Kyllä.
7. Valitse OK.
    * Tarkista luotu tuotos. Ota huomioon, että raportissa esitetään sekä yrityksen logo että valtuutetun henkilön allekirjoitus. Allekirjoituskuva saadaan valittuun pankkitiliin liitetyn sekin asettelutietueen säilön tietotyypin kentästä.  
8. Laajenna Kopiot-osa.
9. Valitse Muokkaa.
10. Syötä Vesileima-kenttään Tulosta vesileimaksi mitätöity.
    * Muuta vesileiman asettelun asetusta niin, että vesileiman teksti näkyy luotavan Excel-muotoisen elementin asiakirjassa.  
11. Valitse Tulosta testi.
12. Valitse OK.
    * Tarkista luotu tuotos. Ota huomioon, että vesileima näytetään luodussa raportissa valinnan asetuksen mukaisesti.  
13. Sulje sivu.
14. Valitse toimintoruudussa Maksujen hallinta.
15. Valitse Sekit.
16. Valitse Näytä suodattimet.
17. Käytä seuraavia suodattimia: Syötä suodattimen arvo "381","385","389" Sekin numero -kenttään. Käytä On yksi seuraavista -suodatinoperaattoria.
18. Merkitse luettelossa kaikki rivit.
19. Valitse Tulosta sekin kopio.
    * Suorita muoto valittujen sekkien uudelleentulostusta varten.  
    * Tarkista luotu tuotos. Ota huomioon, että valitut sekit on tulostettu uudelleen. Yrityksen logoa ja nimiöitä ei tulosteta, koska näkyvät esitäytetyssä lomakkeessa.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Tuodun tietomallin yhdistämismäärityksen muokkaaminen
1. Sulje sivu.
2. Sulje sivu.
3. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
4. Valitse puussa Sekkien malli.
5. Valitse Suunnittelutoiminto.
6. Valitse Yhdistä malli tietolähteeseen.
7. Valitse Suunnittelutoiminto.
    * Tietomallin allekirjoitusnimikkeen sidontaa muutetaan, jotta allekirjoituskuva voidaan hakea valittuun pankkitiliin liitetyn sekin asettelutietueeseen liitetystä asiakirjoista.  
8. Poista Näytä tiedot -kohta käytöstä.
9. Laajenna puussa layout.
10. Laajenna puussa layout\signature.
11. Valitse puussa layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp.
12. Laajenna puussa chequesaccount.
13. Laajenna puussa chequesaccount\<Relations.
14. Laajenna puussa chequesaccount\<Relations\BankChequeLayout.
15. Laajenna puussa chequesaccount\<Relations\BankChequeLayout\<Relations.
16. Laajenna puussa chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents.
17. Valitse puussa chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer().
18. Valitse Sido.
19. Valitse Tallenna.
20. Sulje sivu.
21. Sulje sivu.
22. Sulje sivu.
23. Sulje sivu.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Muodon suorittaminen muokatun mallin yhdistämismäärityksen avulla
1. Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Pankkitili-kenttää arvolla USMF OPER.
3. Valitse toimintoruudussa Määritä.
4. Valitse Tarkista.
5. Valitse Tulosta testi.
6. Valitse OK.
    * Tarkista luotu tuotos. Ota huomioon, että tiedostojen hallinnan liitteen kuva näkyy valtuutetun henkilön allekirjoituksena.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>MS Word -asiakirjan käyttäminen mallina tuodussa muodossa
1. Sulje sivu.
2. Sulje sivu.
3. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
4. Valitse puussa Model for cheques.
5. Valitse puussa Model for cheques\Cheques printing format.
6. Valitse Suunnittelutoiminto.
7. Napsauta Liitteet.
8. Valitse Poista.
9. Valitse Kyllä.
10. Valitse Uusi.
11. Napsauta Tiedosto.
    * Valitse Selaa ja valitse sitten etukäteen ladattu tiedosto nimeltä Cheque template Word.docx.  
12. Sulje sivu.
13. Syötä tai valitse Malli-kentän arvo.
14. Valitse Tallenna.
15. Sulje sivu.
16. Valitse Muokkaa.
17. Valitse Suorita luonnos -kentässä Kyllä.
18. Sulje sivu.
19. Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.
20. Pikasuodattimen avulla voit suodattaa Pankkitili-kentän USMF OPER -arvon mukaan.
21. Valitse Tarkista.
22. Valitse Tulosta testi.
23. Valitse OK.
    * Tarkista luotu tuotos. Ota huomioon, että tuloste on luotu MS Word -asiakirjana, joka sisältää yrityksen logoa esittävät upotetut kuvat, valtuutetun henkilön allekirjoituksen ja vesileiman valitun tekstin.  


