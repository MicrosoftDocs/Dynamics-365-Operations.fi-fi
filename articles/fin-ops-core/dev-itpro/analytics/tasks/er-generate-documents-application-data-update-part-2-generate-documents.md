---
title: Suunnittele konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja
description: Tässä artikkelissa käsitellään sähköisen raportoinnin (ER) määritysten suunnittelua sähköisen asiakirjan luontia varten. (Osa 1 – Konfiguraatioiden tuonti).
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290541"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Suunnittele konfiguraatioita luodaksesi sovellustietoja sisältäviä asiakirjoja

[!include [banner](../../includes/banner.md)]

Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 1: konfiguraatioiden tuominen) -menettely on suoritettu.



Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista varten. Tässä menettelyssä suoritetaan tuotu ER-muotokonfiguraatio, joka on luotu malliyritykselle Litware Inc. sähköisten asiakirjojen luomista varten.



Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla. 



Ennen kuin aloitat, muuta DEMF-yrityksen maakonteksti DEU (Saksa) -arvosta BEL (Belgia) -arvoksi. Valitse Organisaation hallinto > Organisaatiot > Yritykset, kun haluat päivittää yrityksen DEMF ensisijaisen osoitteen maakoodin. Käynnistä sovellus uudelleen.


## <a name="run-imported-er-format"></a>Tuodun ER-muodon suorittaminen
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa Intrastat (model).
3. Valitse puussa Intrastat (model)\Intrastat (format).
4. Valitse Suorita.
    * Suorita ER-muotokonfiguraation luonnosversio, kun haluat luoda Intrastat-raportin.  
5. Kirjoita Syötä tiedostonimi -kenttään intrastat.xml.
    * Anna tiedoston nimi.  
6. Valitse OK.
    * Tarkista luotu XML-tiedosto.  
7. Sulje sivu.
8. Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.
    * Avaa tämä lomake, kun haluat tarkastella luodun sähköisen asiakirjan Intrastat-tapahtumia.  
9. Valitse Intrastat-arkisto.
    * Koska suoritettu ER-muoto ei sisällä sovellustietojen päivityksen asetuksia, valmiin Intrastat-raportin tietoja ei ole arkistoitu.  
10. Sulje sivu.
11. Sulje sivu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
