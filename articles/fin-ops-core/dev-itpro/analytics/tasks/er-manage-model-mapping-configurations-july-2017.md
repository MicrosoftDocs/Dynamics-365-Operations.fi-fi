---
title: Sähköisen raportointimallin kartoituksen hallinta erillisissä sähköisen raportoinnin konfiguraatioissa
description: Tässä artikkelissa käsitellään sähköisen raportoinnin (ER) mallin yhdistämismääritysten hallintaa erillisissä ER-määrityksissä.
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd39ba470a418ca6e4fe7e44b3ae22c8eaa12f9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847250"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a>Hallitse ER-mallien kartoitusta erillisissä ER-konfiguraatioissa

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi hallita sähköisen raportoinnin (ER) mallin yhdistämismäärityksiä erillisissä ER-konfiguraatioissa. Tässä tehtäväoppaassa luodaan pakollisia ER-määrityksiä malliyritykselle Litware, Inc. Tätä tehtäväopastaa varten on suoritettava ensin ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -tehtäväoppaan vaiheet. 

Voit suorittaa tämän tehtäväoppaan valitsemasi yrityksen tietojoukon avulla, koska yritykset jakavat ER-konfiguraatiot. Tässä oppaassa tehtävä toiminto on käytettävissä, jos olet asentanut jonkin seuraavista hotfix-korjauksista: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 Dynamics AX 7.0 -versiolle tai https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 Dynamics 365 for Operations -versiolle.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Tarkista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja onko se merkitty aktiiviseksi. Jos tämän määrityksen tarjoajaa ei ole näkyvissä, tehtäväoppaan vaiheet on suoritettava ensin, Määrityksen tarjoaja on luotava ja se on merkittävä aktiiviseksi.   

## <a name="add-a-new-er-model-configuration"></a>Uuden ER-mallimäärityksen lisääminen
1. Valitse Raportointikonfiguraatiot.
    * Luo uusi mallin konfiguraatio. Konfiguraatioiden puurakenteen nimen on oltava yksilöivä.  
2. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
3. Syötä Nimi-kenttään Tietomallin esimerkki.
    * Tietomallin esimerkki  
4. Valitse Luo konfiguraatio.
5. Valitse Suunnittelutoiminto.
6. Avaa valintaikkuna valitsemalla Uusi.
7. Kirjoita Nimi-kenttään "Juuri".
    * Juuri  
8. ValitseLisää.
9. Avaa valintaikkuna valitsemalla Uusi.
10. Syötä Nimi-kenttään Yritys.
    * Yritys   
11. ValitseLisää.
12. Syötä Kuvaus-kenttään teksti, yrityksen kuvaus tai yritys, johon käyttäjä oli kirjautuneena suorituksen aikana. 
    * Sen yrityksen kuvaus, johon käyttäjä on kirjautuneena suorituksen aikana.  
13. Valitse Juuriviite.
14. Valitse OK.
15. Valitse Tallenna.
16. Sulje sivu.
17. Voit muuttaa tilaa valitsemalla Muuta.
18. Valitse Valmis.
19. Valitse OK.

## <a name="add-a-new-er-model-mapping-configuration"></a>Uuden ER-mallin yhdistämismääritysmäärityksen lisääminen
1. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
2. Anna Uusi-kenttään Mallin yhdistämismääritys perustuu tietomalliin Tietomallin esimerkki.
3. Syötä Nimi-kenttään Esimerkkiyhdistämismääritys.
    * Esimerkkiyhdistämismääritys  
4. Valitse Luo konfiguraatio.
5. Laajenna Edellytykset-osa.
    * Toteutusten edellytysten ryhmä on lisätty automaattisesti. Ryhmä sisältää edellytetyn komponentin, joka viittaa päätietomallin konfiguraatioon ja jossa käytetään Toteutus-merkintää. Tämä tarkoittaa, että Esimerkkiyhdistämismääritys-yhdistämismäärityksen konfiguraatiota pidetään Esimerkki-tietomallin toteutuksena. Tämä vuoksi tämä komponentti pakottaa sähköisen raportoinnin lataamaan mallin yhdistämismäärityksen määrityksen (Esimerkkiyhdistämismääritys) sähköisen raportoinnin säilöstä, kun mallin määritys, Esimerkkitietomalli, ladataan.   
6. Valitse Suunnittelutoiminto.
    * Luotu mallin yhdistämismäärityksen kokoonpano sisältää uuden tyhjän yhdistämismäärityksen, jolla on sama nimi kuin luodulla määrityksellä. Kun valittu päämallin määritys sisältää mallin yhdistämismäärityksiä, ne kopioidaan uuteen mallin yhdistämismäärityksen määritykseen.   
7. Valitse Suunnittelutoiminto.
8. Valitse puussa Dynamics 365 for Operations\Table.
9. Valitse Lisää juuri.
10. Syötä Nimi-kenttään Yritys.
    * Yritys   
11. Syötä Taulu-kenttään CompanyInfo.
    * CompanyInfo  
12. Valitse OK.
13. Laajenna puussa Company.
14. Laajenna puussa Company\find().
15. Valitse puussa Company\find()\Name.
16. Valitse Sido.
17. Valitse Tallenna.
18. Sulje sivu.
19. Sulje sivu.
20. Valitse toimintoruudussa Konfiguroinnit.
21. Valitse Käyttäjän parametrit.
22. Valitse Suorita asetukset -kentässä Kyllä.
23. Valitse OK.
24. Valitse Muokkaa.
25. Valitse Suorita luonnos -kentässä Kyllä.

## <a name="add-a-new-er-format-configuration"></a>Uuden ER-muotokonfiguraation lisääminen
1. Valitse puussa Sample data model.
2. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
3. Anna Uusi-kenttään Muoto perustuu tietomalliin Tietomallin esimerkki.
4. Syötä Nimi-kenttään Esimerkkimuoto.
    * Esimerkkimuoto  
5. Valitse Luo konfiguraatio.
6. Valitse Suunnittelutoiminto.
7. Avaa valintaikkuna valitsemalla Lisää juuri.
8. Valitse puussa solmu Text\String.
9. Valitse OK.
10. Valitse Yhdistämismääritys-välilehti.
11. Laajenna puussa solmu model.
12. Valitse puussa model\Company.
13. Valitse Sido.
14. Valitse Tallenna.
15. Sulje sivu.
    * Suorita luodun muodon luonnosversio testausta varten.  
16. Valitse Suorita.
    * Valitse Versiot-pikavälilehdessä Suorita.  
17. Valitse OK.
    * Tarkista tulos, joka sisältää sen yrityksen nimen, johon tämän muotokonfiguraation suorittava käyttäjä on kirjautunut. Luotu muotomääritys käyttää tätä mallin yhdistämismäärityksen määritystä, koska vaaditut mallin yhdistämismääritykset sisältäviä määrityksiä on vain yksi.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Vaihtoehtoisen ER-mallin yhdistämismäärityksen määrityksen lisääminen
1. Valitse puussa Sample data model.
2. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
3. Anna Uusi-kenttään Mallin yhdistämismääritys perustuu tietomalliin Tietomallin esimerkki.
4. Syötä Nimi-kenttään Esimerkkiyhdistämismääritys (vaihtoehto).
    * Esimerkkiyhdistämismääritys (vaihtoehto)  
5. Valitse Luo konfiguraatio.
6. Valitse Suunnittelutoiminto.
7. Valitse Suunnittelutoiminto.
8. Valitse puussa Dynamics 365 for Operations\Table.
9. Valitse Lisää juuri.
10. Syötä Nimi-kenttään Yritys.
    * Yritys   
11. Syötä Taulu-kenttään CompanyInfo.
    * CompanyInfo  
12. Valitse OK.
13. Valitse Muokkaa.
14. Valitse puussa solmu String\CONCATENATE.
15. Valitse Lisää toiminto.
16. Laajenna puussa Company.
17. Laajenna puussa Company\find().
18. Valitse puussa Company\find()\Name.
19. Valitse Lisää tietolähde.
20. Kirjoita arvo Resepti-kenttään.
    * CONCATENATE(Company.'find()'.Name, ";",  
21. Valitse puussa Company\find()\Company(DataArea).
22. Valitse Lisää tietolähde.
23. Kirjoita arvo Resepti-kenttään.
    * CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)  
24. Valitse Tallenna.
25. Sulje sivu.
26. Valitse Tallenna.
27. Sulje sivu.
28. Sulje sivu.
29. Valitse Suorita luonnos -kentässä Kyllä.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Aiemmin määritetyn ER-mallin yhdistämismäärityksen määrityksen käyttäminen
1. Valitse puussa Sample data model\Sample format.
2. Valitse Suorita.
    * Valittua ER-muotokonfiguraation luonnosversiota ei voi suorittaa, koska suoritettavan ER-muodon tietolähteeksi valitulla määrittämättömällä tietomallilla on käytettävissä useita mallin yhdistämismäärityksen määrityksiä.   
    * Seuraavaksi määritetään vaihtoehtoinen mallin yhdistämismäärityksen määritys, josta mallin yhdistämismäärityksiä käytetään tietolähteinä ER-muodon suorituksessa.   
3. Valitse puussa Sample data model\Sample mapping (alternative).
4. Valitse Mallin määrityksen oletusarvo -kentässä Kyllä.
5. Valitse puussa Sample data model\Sample format.
6. Valitse Suorita.
7. Valitse OK.
    * Tämä mallin yhdistämismäärityksen määritys käyttää mallin yhdistämismäärityksen oletusmääritystä sähköisen asiakirjan (luotu tuloste sisältää yrityskoodin) luomiseen.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]