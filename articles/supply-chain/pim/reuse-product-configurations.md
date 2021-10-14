---
title: Tuotekonfiguraatioiden käyttäminen uudelleen
description: Voit määrittää, että haluat uudelleenkäyttää automaattisesti tuotteen aiemmin luotua konfiguraatiota. Kun käyttäjän määritysistunto on valmis, järjestelmä tarkistaa, onko käyttäjän valintoja vastaava konfiguraatio jo olemassa. Jos vastaava konfiguraatio löytyy, konfiguraatiotunnusta, vastaavaa tuoterakennetta ja reititystä käytetään uudelleen.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0898bd1832fa7007fc3aa265beee2e930f157a39
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577405"
---
# <a name="reuse-product-configurations"></a>Tuotekonfiguraatioiden käyttäminen uudelleen

[!include [banner](../includes/banner.md)]

Voit määrittää, että haluat uudelleenkäyttää automaattisesti tuotteen aiemmin luotua konfiguraatiota. Kun käyttäjän määritysistunto on valmis, järjestelmä tarkistaa, onko käyttäjän valintoja vastaava konfiguraatio jo olemassa. Jos vastaava konfiguraatio löytyy, konfiguraatiotunnusta, vastaavaa tuoterakennetta ja reititystä käytetään uudelleen.

## <a name="requirements-for-reusing-configurations"></a>Konfiguraatioiden uudelleenkäytön vaatimukset

Konfiguraatioiden uudelleenkäyttöä varten on määritettävä seuraavat komponenttien ja ominaisuuksien tiedot **Tuotemääritysmallin tietoja** -sivulla:

-   **Komponentit ja alikomponentit** – Valitse **yleiset** pikavälilehden **Käytä konfiguraatioita** -kentässä **Kyllä**.
-   **Määritteet** – Valitse **määritteet** pikavälilehdessä **Sisällytä uudelleenkäyttöön** -vaihtoehto. Tämä vaihtoehto on käytettävissä vain, kun liittyvä komponentti on määritetty uudelleenkäyttöä varten. Jos et valitse mitään uudelleenkäytön määritteitä, konfiguraatiota käytetään aina uudelleen, riippumatta käyttäjän valinnoista määritysistunnon aikana. Käytössä olevien konfiguraatioiden määritteiden arvojen  on vastattava käyttäjän valintoja, Jos käyttäjä esimerkiksi valitsee **sininen** väriksi määritysistunnossa, järjestelmä tarkistaa, onko aiemmin luodun komponentin konfiguraatiossa sininen väri.

## <a name="resetting-configuration-reuse"></a>Konfiguraation uudelleenkäytön nollaaminen
Kun nollaat konfiguroinnin uudelleenkäytön, aiemmin luotuja konfiguraatioita ei enää käsitellä. Voit halutessasi nollata konfiguroinnin uudelleenkäytön, jos tuoterakennetta tai reititystä on muutettu, mutta niihin liittyviä määritteitä ei ole muutettu. Konfiguroinnin uudelleenkäyttö nollataan kohdassa **yleiset** komponentin pikavälilehdessä.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]