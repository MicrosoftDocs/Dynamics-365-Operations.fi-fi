---
title: Asiakasmaksujen tiedot (esiversio)
description: Täsäs ohjeaiheessa kerrotaan maksun tietojen ominaisuudesta. Sen avulla saadaan lisätietoja yksittäisten asiakkaiden tyypillistä maksukäytännöistä. Tämän toiminnon avulla voit myös määrittää olosuhteet, joiden vuoksi perintäprosessit voidaan aloittaa tapauksissa, joissa muuten et niin tekisi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d01f15223b4665caec16d6a4e51a5121a0ed94ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012161"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="98e6e-104">Asiakasmaksujen tiedot (esiversio)</span><span class="sxs-lookup"><span data-stu-id="98e6e-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="98e6e-105">Täsäs ohjeaiheessa kerrotaan maksun tietojen ominaisuudesta. Sen avulla saadaan lisätietoja yksittäisten asiakkaiden tyypillistä maksukäytännöistä.</span><span class="sxs-lookup"><span data-stu-id="98e6e-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="98e6e-106">Tämän toiminnon avulla voit myös määrittää olosuhteet, joiden vuoksi perintäprosessit voidaan aloittaa tapauksissa, joissa muuten et niin tekisi.</span><span class="sxs-lookup"><span data-stu-id="98e6e-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="98e6e-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="98e6e-107">Overview</span></span>

<span data-ttu-id="98e6e-108">Joskus voi olla haastavaa ennustaa, milloin asiakkaat maksavat laskut.</span><span class="sxs-lookup"><span data-stu-id="98e6e-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="98e6e-109">Tämän tiedon puute heikentää kassavirtaennusteiden tarkkuutta sekä johtaa liian myöhään käynnistyviin perintäprosesseihin ja tilausten vapauttamiseen asiakkaille, jotka voivat jättää laskut maksamatta.</span><span class="sxs-lookup"><span data-stu-id="98e6e-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="98e6e-110">Asiakkaan maksujen tiedot (esiversio) auttaa organisaatioita ennustamaan, milloin myyntilasku maksetaan.</span><span class="sxs-lookup"><span data-stu-id="98e6e-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="98e6e-111">Näiden tietojen avulla organisaatiot voivat luoda perintästrategioita, jotka parantavat ajoissa maksettavan maksun todennäköisyyttä.</span><span class="sxs-lookup"><span data-stu-id="98e6e-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="98e6e-112">Ennusteet</span><span class="sxs-lookup"><span data-stu-id="98e6e-112">Predictions</span></span>

<span data-ttu-id="98e6e-113">Maksuennusteiden avulla organisaatiot voivat parantaa liiketoimintaprosesseja, sillä organisaatioiden on helppo tunnistaa laskut, joiden maksu todennäköisesti myöhästyy. Lisäksi organisaatiot voivat käyttöön toimenpiteitä, jotka parantavat todennäköisyyttä, että maksu maksetaan ajoissa.</span><span class="sxs-lookup"><span data-stu-id="98e6e-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="98e6e-114">Asiakasmaksujen tiedot (esiversio) käyttää historiallisia laskuja, maksuja ja asiakastietoja hyödyntävää koneoppimismallia, mikä tarkentaa sen ennustamista, milloin asiakas maksaa jäljellä olevan laskun.</span><span class="sxs-lookup"><span data-stu-id="98e6e-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="98e6e-115">Asiakkaan maksutavat (esiversio) voi ennustaa kolme maksun todennäköisyyttä kullekin avoimelle laskulle:</span><span class="sxs-lookup"><span data-stu-id="98e6e-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="98e6e-116">Todennäköisyys sille, että maksu suoritetaan ajoissa</span><span class="sxs-lookup"><span data-stu-id="98e6e-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="98e6e-117">Todennäköisyys sille, että maksu suoritetaan myöhässä</span><span class="sxs-lookup"><span data-stu-id="98e6e-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="98e6e-118">Todennäköisyys sille, että maksu suoritetaan erittäin paljon myöhässä</span><span class="sxs-lookup"><span data-stu-id="98e6e-118">Probability of payment being made very late</span></span>

<span data-ttu-id="98e6e-119">Asiakasmaksujen tiedot (esiversio) -toiminnossa on myös koostenäkymä odotetuista maksuista. Sen avulla organisaatiot saavat paremman käsityksen siitä maksun kokonaissummasta, jonka ne voivat odottaa asiakkaan maksavan, sen perusteella, mihin jaksoon asiakas sijoittuu (ajoissa, myöhässä ja erittäin paljon myöhässä).</span><span class="sxs-lookup"><span data-stu-id="98e6e-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="98e6e-120">[![Maksuennusteiden koostenäkymä](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="98e6e-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="98e6e-121">Lisäksi kullekin laskulle määritetään todennäköisyys ajoissa maksamisesta.</span><span class="sxs-lookup"><span data-stu-id="98e6e-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="98e6e-122">Jos maksun todennäköisyys on alle 50 %, laskuihin lisätään punainen ympyrä osoittamaan, että lasku on ehkä lähetettävä perintään.</span><span class="sxs-lookup"><span data-stu-id="98e6e-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="98e6e-123">[![Maksun todennäköisyyksien luettelo](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="98e6e-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="98e6e-124">Asiakasmaksujen tiedot (esiversio) sisältää myös kontekstitietoja, jotka selventävät ennustetta. Niitä ovat esimerkiksi tärkeimmät ennusteeseen vaikuttaneet seikat, asiakkaan liikesuhteen nykyinen tila ja asiakkaan historialliset maksutiedot.</span><span class="sxs-lookup"><span data-stu-id="98e6e-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="98e6e-125">Monissa yrityksissä perintäprosessi on reaktiivista, jolloin perintäprosessi alkaa vasta, kun laskut erääntyvät.</span><span class="sxs-lookup"><span data-stu-id="98e6e-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="98e6e-126">Asiakasmaksujen tiedot (esiversio) antaa organisaatioille mahdollisuuden toimia perinnän suhteen ennakoivasti.</span><span class="sxs-lookup"><span data-stu-id="98e6e-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="98e6e-127">Niiden ei enää tarvitse odottaa, että tapahtuvat erääntyvät ennen perintäprosessin aloittamista.</span><span class="sxs-lookup"><span data-stu-id="98e6e-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="98e6e-128">Sen sijaan ne voivat selvittää maksuennusteominaisuuden avulla, parantaako ennakkoiva perintä todennäköisyyttä ajoissa tapahtuvasta maksun maksamisesta.</span><span class="sxs-lookup"><span data-stu-id="98e6e-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="98e6e-129">Yritykset saavat maksuennusteen avulla myös tietoja, joita ne tarvitsevat perustelemaan etukäteen aloitettavaa perintäprosessia.</span><span class="sxs-lookup"><span data-stu-id="98e6e-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="98e6e-130">Metodologia</span><span class="sxs-lookup"><span data-stu-id="98e6e-130">Methodology</span></span>

<span data-ttu-id="98e6e-131">Tekoälyratkaisun kehittäminen ja käyttöönotto on vaikeaa.</span><span class="sxs-lookup"><span data-stu-id="98e6e-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="98e6e-132">Sitä varten tarvitaan ryhmä, jossa on datatieteilijöitä, aihealueen asiantuntijoita ja teknikoita, jotka käyttävät paljon aikaa käyttökelpoisen tekoälyratkaisun muotoiluun, kehittämiseen, käyttöönottamiseen ja ylläpitoon.</span><span class="sxs-lookup"><span data-stu-id="98e6e-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="98e6e-133">Tekoälyratkaisujen käyttöönottaminen ja käyttö Financessa on kuitenkin helppoa.</span><span class="sxs-lookup"><span data-stu-id="98e6e-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="98e6e-134">Finance sisältää valmiiksi pakattuja tekoälyratkaisuja, jotka on muodostettu Microsoft AI Builderin pohjalta.</span><span class="sxs-lookup"><span data-stu-id="98e6e-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="98e6e-135">Loppukäyttäjä voi ottaa yhdellä napsautuksella käyttöön tekoälyratkaisun ja aloittaa älykkäistä ennusteista saatavien etujen hyödyntämisen.</span><span class="sxs-lookup"><span data-stu-id="98e6e-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="98e6e-136">Jos organisaatio ei ole tyytyväinen ennusteiden tarkkuuteen, tehokäyttäjä voi lisätä taas yhdellä napsautuksella AI Builderin laajennuskokemuksen ja sitten valita ennusteiden muodostamiseen käytettäviä kenttiä tai poistaa niiden valinnan.</span><span class="sxs-lookup"><span data-stu-id="98e6e-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="98e6e-137">Kun muutokset on tehty, muutokset voidaan kouluttaa ja julkaista, minkä jälkeen uusi koulutettu malli valitaan Financessa automaattisesti ennusteisiin.</span><span class="sxs-lookup"><span data-stu-id="98e6e-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="98e6e-138">Asiakasmaksujen tiedot (esiversio) -toiminnon hankkiminen</span><span class="sxs-lookup"><span data-stu-id="98e6e-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="98e6e-139">Lähetä sähköpostia osoitteeseen [Asiakasmaksujen tiedot (esiversio)](mailto:fiap@microsoft.com), jos haluat kokeilla Asiakasmaksun tiedot (esiversio) -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="98e6e-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="98e6e-140">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="98e6e-140">Privacy Notice</span></span>

<span data-ttu-id="98e6e-141">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="98e6e-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


