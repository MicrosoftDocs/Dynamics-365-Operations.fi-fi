---
title: Tehtävien määrittäminen tehtävienhallinnassa
description: Tässä artikkelissa kerrotaan, kuinka voit määrittää tehtäviä Microsoft Dynamics 365 Human Resourcesin tehtävienhallinnassa.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745385"
---
# <a name="set-up-tasks-in-task-management"></a>Tehtävien määrittäminen tehtävienhallinnassa

[!INCLUDE [PEAP](../includes/peap-1.md)]

Microsoft Dynamics 365 Human Resources -versiota 10.0.30 edeltävissä versioissa käyttäjien täytyi muokata tehtäviä erikseen jokaisessa tarkistusluettelossa, joka sisälsi kyseisen tehtävän. Human Resources -versiosta 10.0.30 alkaen käyttäjät voivat kuitenkin valita, miten muokatut tehtävät käsitellään. Jos muokattava tehtävä sisältyy tarkistusluetteloon, **Ota tehtävien hallinnan ohjelmistopäivitys käyttöön** -vaihtoehdon täytyy olla valittuna **Henkilöstöhallinnon jaetut parametrit** -sivun **Tehtävänhallinta**-välilehdessä, jotta tarkistusluettelo voi käyttää muokattua tehtävää.

[![Ota tehtävien hallinnan ohjelmistopäivitys käyttöön -vaihtoehto Henkilöstöhallinnon jaetut parametrit -sivulla.](./media/task-update.png)](./media/task-update.png)

Jos tehtävien muutokset tulisi ottaa käyttöön kaikissa tarkistusluettelon tehtävissä, tehtäväkirjastossa olevan tehtävän ja tarkistusluettelossa olevan tehtävän välillä on oltava jo suhde. Lisäsimme vaihtoehdon, jolla kirjaston tehtävän ja tarkistusluettelon tehtävän välille voi luoda suhteen.

Voit luoda tehtävät yksitellen ja käyttää niitä uudelleen useissa tarkistusluetteloissa. Voit luoda tehtävän valitsemalla **Perehdytyksen asetukset** -sivun **Tehtävät**-välilehdessä **Uusi**.

## <a name="set-up-tasks"></a>Tehtävien määrittäminen

Jos haluat kohdistaa luodun tehtävän useisiin tarkistusluetteloihin, valitse tehtävä ja valitse sitten valikosta **Kohdista tarkistusluetteloihin**.

Voit myös lisätä tehtäviä suoraan tarkistusluetteloon. Voit lisätä tehtävän tarkistusluetteloon luomalla **Perehdytyksen asetukset** -sivun **Tarkistusluettelo**-välilehdestä uuden tarkistusluettelon, johon tehtävä lisätään, tai lisätä tehtävän aiemmin luotuun tarkistusluetteloon.

Jos haluat muokata kirjastossa olevaa tehtävää, valitse tehtäväkirjaston valikosta **Muokkaa**. Jos tehtävä on liitetty tarkistusluetteloihin, nämä tarkistusluettelot näkyvät **Muokkaa tehtävää** -sivulla. Jos haluat, että jonkin tarkistusluettelon tehtävät päivitetään muutosten mukaisesti, valitse kyseiset tarkistusluettelot **Kohdista tarkistusluetteloihin** -osiosta.

Voit poistaa tehtäviä tehtäväkirjastosta valitsemalla **Poista**. Jos tehtävä liittyy tarkistusluetteloon, tämä toiminto ei poista tehtävää tarkistusluettelosta. Tehtävä täytyy poistaa tarkistusluettelosta erillisellä toiminnolla.

### <a name="set-up-checklists"></a>Tarkistusluetteloiden määrittäminen

Tarkistusluettelo on tehtäväryhmä. Voit luoda niin monta tarkistusluetteloa kuin on tarpeen, ja voit määrittää samat tehtävät useisiin tarkistusluetteloihin. Kun luot tarkistusluettelon, määrität omistajan ja kalenterin.

Jos haluat luoda tarkistusluetteloon uuden tehtävän, valitse tehtävien valikkoriviltä **Uusi**. Kun luot uuden tehtävän, voit lisätä sen halutessasi tehtäväkirjastoon, jotta se voidaan jakaa moniin eri tarkistusluetteloihin. Jos haluat lisätä tehtävän tehtävänkirjastoon, sinun täytyy määrittää **Kohdista tehtävä kirjastoon** -vaihtoehdoksi **Kyllä**. Jos päätät lisätä tehtävän tehtäväkirjastoon, voit lisätä sen samalla myös muihin tarkistusluetteloihin valitsemalla tarkistusluettelot **Kohdista tarkistusluetteloihin** -osiosta. Jos päätät olla lisäämättä tehtävää tehtäväkirjastoon, se on olemassa vain tarkistusluettelossa, jossa loit sen.

Jos haluat muokata tarkistusluettelossa olevaa tehtävää, valitse tehtävän valikosta **Muokkaa**. Jos tehtävä on liitetty tarkistusluetteloihin, nämä tarkistusluettelot näkyvät **Muokkaa tehtävää** -sivulla. Jos haluat, että joidenkin muiden tarkistusluetteloiden tehtävät päivitetään muutosten mukaisesti, valitse kyseiset tarkistusluettelot **Kohdista tarkistusluetteloihin** -osiosta.

Jos haluat poistaa tehtäviä tarkistusluettelosta, valitse **Poista**. Tämä toiminto poistaa tehtävät tarkistusluettelosta. Se ei kuitenkaan poista tehtäviä pysyvästi tehtäväkirjastosta. Jos haluat poistaa tehtäviä pysyvästi tehtäväkirjastosta, avaa **Tehtäväkirjasto**-sivu ja valitse **Poista**.
