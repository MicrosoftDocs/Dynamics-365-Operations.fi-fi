---
title: Syötä osaamisalueet
description: Työt ja esimiehet voivat syöttää osaamisalueita Dynamics 365 Human Resourcesiin.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 8a6b36314d9d98f971cd1619dd3604f20a3770b3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360517"
---
# <a name="enter-skills"></a>Syötä osaamisalueet

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Määritä tavoite- tai todelliset osaamisalueet työntekijöille, hakijoille tai yhteyshenkilöille Dynamics 365 Human Resourcesissa. Tavoitetaito on taito, jonka henkilö aikoo saavuttavansa. Todellisella osaamisalueella tarkoitetaan osaamista, jonka henkilöllä tällä hetkellä on.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Osaamisalueiden automaattisen hyväksymisen työnkulun luominen

Jos haluat määrittää osaamisalueita ilman hyväksyntää, sinun on luotava työnkulku osaamisalueiden automaattista hyväksymistä varten.

> [!NOTE]
> Työntekijöiden syötetyt osaamisalueet edellyttävät aina esimiehen hyväksyntää. Tämä työnkulku hyväksyy vain esimiesten työntekijöiden puolesta syötetyt osaamisalueet automaattisesti.

1. Valitse **Henkilöstön hallinta** -työtilassa **Linkit**.

2. Valitse **Määritys**-kohdasta **Henkilöstöhallinnon työnkulut**.

3. Valitse **Uusi**.

4. Valitse **Luo työnkulku** -ruudusta **Työntekijän osaamisalueet**.

   [![Työntekijän osaamisalueet -työnkulun valinta.](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. Valitse **Avataanko tämä tiedosto** -valintaruudusta **Avaa**. Kirjoita tunnistetietosi, kun näet kehotteen.

6. Valitse työnkulun editorissa **Hyväksy osaamisalueet** -työnkulun elementti ja vedä se pohjaan perustuvaan sovellukseen.

   [![Valitse Hyväksy osaamisalueet -työnkulkuelementti.](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Liitä **Aloitus**-elementti **Hyväksy osaamisalueet 1** -elementtiin ja liitä sitten **Hyväksy osaamisalueet 1** -elementti **Loppu**-elementtiin. Sinun on ehkä siirryttävä alaspäin, jos haluat nähdä **Loppu**-elementin. Voit vetää sitä lähemmäksi muita elementtejä.

   [![Yhdistä työnkulun elementit.](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Kaksoisnapsauta **Hyväksy osaamisalueet 1** -työnkulkuelementtiä ja napsauta **vaiheen 1** elementtiä hiiren kakkospainikkeella. Napsauta **vaiheen 1** elementtiä hiiren kakkospainikkeella ja valitse **Ominaisuudet**.

9. Valitse **Ominaisuudet**-ikkunasta **Ehto** vasemmanpuoleisessa siirtymispalkissa.

10. Valitse **Suorita tämä vaihe vain, kun seuraava ehto täyttyy**.

11. Valitse **Lisää ehto**. Valitse **Missä**-ehdon jälkeen **Työntekijän itsepalvelun osaamisalueet** ja valitse sitten **Työntekijän itsepalvelun osaamisalueet.Henkilö**. Valitse arvon **on** jälkeen **kenttä** ja valitse sitten **Käyttäjä suhteeseen.Henkilö**.

    [![Määritä ehto.](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Valitse **Määritys** vasemmalla puolella olevasta valikosta.

13. Valitse **Hierarkia** **Määrityksen tyyppi** -välilehdestä.

14. Valitse **Hierarkian valinta** -välilehden **Hierarkiatyyppi:** -kentässä **Hallintahierarkia**.

    [![Hallintahierarkian asetukset.](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Valitse **Sulje**, valitse **Työnkulku** kaavan polusta ja valitse sitten **Tallenna ja sulje**.

Lisätietoja työnkulkujen luomisesta on kohdassa [Työnkulkujärjestelmän yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Työntekijän osaamisalueille syötetyt tiedot

1. Valitse työntekijä.

2. Valitse **Työntekijä**-sivun toimintopalkissa **Henkilö** ja valitse sitten **Osaamisalueet**.

3. Täytä **Osaamisalueet**-sivulla kunkin osaamisalueen kentät:

   - **Osaamisalue**: Valitse osaamisalue.
   - **Tasotyyppi**: Valitse **osaamisalue**, joka työntekijällä on jo, tai valitse sen osaamisalueen **kohde**, jolla työntekijä työskentelee.
   - **Taso**: Valitse työntekijän osaamisalueen taso.
   - **Tason päivämäärä**: Valitse päivämäärä kalenterityökalussa.
   - **Tarkastaja**: Valitse tarvittaessa tarkastaja luettelosta. Voit suodattaa hakusi.
   - **Kokemusvuodet**: Syötä kokemusvuodet.
   - **Vahvistettu**: Jos osaamisalue vahvistetaan, valitse tämä valintaruutu.
   - **Vahvistanut**: Kirjoita todentajan nimi.

4. Kun olet syöttänyt osaamisalueet, valitse **Tallenna**.

## <a name="see-also"></a>Lisätietoja

[Osaamisalueiden määritykset](hr-develop-skills.md)<br>
[Osaamisalueiden kartoitus](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]