---
title: ใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าที่คุณต้องดำเนินการให้เสร็จสมบูรณ์เพื่อให้สามารถป้อนหรือนำเข้าข้อมูลภายนอกเข้าในการคาดการณ์กระแสเงินสดได้
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186701"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="c2035-103">ใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="c2035-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c2035-104">คุณสามารถป้อนหรือนำเข้าข้อมูลภายนอกเข้าในการคาดการณ์กระแสเงินสดได้</span><span class="sxs-lookup"><span data-stu-id="c2035-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="c2035-105">หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าที่เกี่ยวข้องกับการใช้ข้อมูลภายนอกโดยเฉพาะและเปิดใช้งานข้อมูลภายนอกที่จะรวมไว้ในการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="c2035-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="c2035-106">การตั้งค่าข้อมูลจากภายนอก</span><span class="sxs-lookup"><span data-stu-id="c2035-106">External data setup</span></span>

<span data-ttu-id="c2035-107">ใช้แท็บ **แหล่งที่มาภายนอก** ในหน้า **การตั้งค่าการคาดการณ์กระแสเงินสด** (**การจัดการเงินสดและธนาคาร \> การคาดการณ์กระแสเงินสด**) เพื่อป้อนการตั้งค่าที่สนับสนุนการใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="c2035-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="c2035-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่า ให้ดูที่ [การคาดการณ์กระแสเงินสด](../cash-bank-management/cash-flow-forecasting.md)</span><span class="sxs-lookup"><span data-stu-id="c2035-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="c2035-109">เมื่อต้องการป้อนข้อมูลภายนอกสำหรับการคาดการณ์กระแสเงินสด คุณสามารถใช้ประสบการณ์เปิดใน Excel สำหรับการป้อนและการปรับเปลี่ยนข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="c2035-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="c2035-110">เลือกปุ่ม **ข้อมูลภายนอก** แล้วเลือก **เพิ่มข้อมูลภายนอก** หรือ **แก้ไขข้อมูลภายนอกที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="c2035-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="c2035-111">เมื่อ Microsoft Excel เปิดไฟล์แล้ว คุณสามารถป้อนข้อมูลในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c2035-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="c2035-112">**รหัสรายการ**</span><span class="sxs-lookup"><span data-stu-id="c2035-112">**Entry ID**</span></span>
- <span data-ttu-id="c2035-113">**คำอธิบาย** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="c2035-113">**Description** (optional)</span></span>
- <span data-ttu-id="c2035-114">**ชื่อแหล่งที่มาภายนอก** – เลือกค่าใดค่าหนึ่งในรายการที่คุณได้กำหนดไว้เมื่อคุณตั้งค่าข้อมูลเชิงลึกทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c2035-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="c2035-115">**นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="c2035-115">**Legal Entity**</span></span>
- <span data-ttu-id="c2035-116">**วัน เดือน**</span><span class="sxs-lookup"><span data-stu-id="c2035-116">**Date**</span></span>
- <span data-ttu-id="c2035-117">**จำนวนเงินในสกุลเงินของธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="c2035-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="c2035-118">**รหัสสกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="c2035-118">**Currency Code**</span></span>
- <span data-ttu-id="c2035-119">**มิติเริ่มต้น** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="c2035-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="c2035-120">**หมายเลขเอกสาร** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="c2035-120">**Document number** (optional)</span></span>
- <span data-ttu-id="c2035-121">**หมายเลขบัญชี** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="c2035-121">**Account number** (optional)</span></span>
- <span data-ttu-id="c2035-122">**ชื่อบัญชี** (ไม่จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="c2035-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="c2035-123">การนำเข้าข้อมูลภายนอกโดยใช้กรอบงานการจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c2035-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="c2035-124">คุณสามารถนำเข้าข้อมูลภายนอกสำหรับการคาดการณ์กระแสเงินสดโดยใช้พื้นที่ทำงาน **การจัดการข้อมูล** และเอนทิตีที่มีการตั้งชื่อ **การคาดการณ์กระแสเงินสดสำหรับการคาดการณ์กระแสเงินสด**</span><span class="sxs-lookup"><span data-stu-id="c2035-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="c2035-125">นอกจากนี้ ถ้าคุณต้องการย้ายข้อมูลการตั้งค่าจากสภาพแวดล้อมหนึ่งไปยังอีกพื้นที่หนึ่ง เอนทิตีที่พร้อมใช้งานสำหรับตารางการตั้งค่าที่จำเป็นต้องใช้:</span><span class="sxs-lookup"><span data-stu-id="c2035-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="c2035-126">การตั้งค่าแหล่งที่มาภายนอกของการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="c2035-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="c2035-127">การตั้งค่านิติบุคคลที่เป็นแหล่งที่มาภายนอกของการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="c2035-127">Cash flow forecast external source legal entity setup</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
