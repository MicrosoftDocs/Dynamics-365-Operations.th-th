---
title: ตั้งค่าสภาพแวดล้อมการพัฒนาอีคอมเมิร์ซ เพื่อดีบักเทียบกับเครื่องเสมือนเซิร์ฟเวอร์ขายปลีกระดับ 1
description: หัวข้อนี้อธิบายวิธีการตั้งค่าสภาพแวดล้อมการพัฒนาอีคอมเมิร์ซ เพื่อดีบักเทียบกับเครื่องเสมือน (VM) เซิร์ฟเวอร์ขายปลีกระดับ 1
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35380a559a4f1b22bdf04ff25cb2bbfc51aff45b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585546"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="dcc8d-103">ตั้งค่าสภาพแวดล้อมการพัฒนาอีคอมเมิร์ซ เพื่อดีบักเทียบกับเครื่องเสมือนเซิร์ฟเวอร์ขายปลีกระดับ 1</span><span class="sxs-lookup"><span data-stu-id="dcc8d-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcc8d-104">หัวข้อนี้อธิบายวิธีการตั้งค่าสภาพแวดล้อมการพัฒนาอีคอมเมิร์ซ เพื่อดีบักเทียบกับเครื่องเสมือน (VM) เซิร์ฟเวอร์ขายปลีกระดับ 1</span><span class="sxs-lookup"><span data-stu-id="dcc8d-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="dcc8d-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="dcc8d-105">Description</span></span>

<span data-ttu-id="dcc8d-106">โดยทั่วไปสภาพแวดล้อม Microsoft Dynamics 365 Commerce ระดับ 1 จะมีการปรับใช้กับ Commerce Runtime (CRT) และการพัฒนาส่วนขยายของการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="dcc8d-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="dcc8d-107">สภาพแวดล้อมแบบสแตนด์อโลน</span><span class="sxs-lookup"><span data-stu-id="dcc8d-107">They are standalone environments.</span></span> <span data-ttu-id="dcc8d-108">เนื่องจากลักษณะของสถาปัตยกรรมซอฟต์แวร์เป็นลักษณะบริการ (SaaS) จึงไม่มีส่วนประกอบของอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="dcc8d-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="dcc8d-109">ในบางสถานการณ์ คุณอาจต้องการทดสอบการเรียกไปยังส่วนขยายในสภาพแวดล้อมระดับ 1 เพื่อให้คุณสามารถดีบักส่วนขยายจากส่วนประกอบอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="dcc8d-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="dcc8d-110">สำหรับคำแนะนำทั่วไป โปรดดู [ดีบักสภาพแวดล้อมการพัฒนา Commerce ระดับ 1](../e-commerce-extensibility/debug-tier-1.md)</span><span class="sxs-lookup"><span data-stu-id="dcc8d-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="dcc8d-111">เมื่อคุณดีบักเทียบกับสภาพแวดล้อมระดับ 1 เนื่องจากไซต์ขณะนี้เรียก Retail Server อื่น การเรียกระหว่างเซิร์ฟเวอร์อาจทําให้เกิดข้อผิดพลาดต่างๆ ที่เกี่ยวข้องกับนโยบายความปลอดภัยของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="dcc8d-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="dcc8d-112">รูปภาพประกอบต่อไปนี้แสดงตัวอย่างข้อผิดพลาดที่อาจเกิดขึ้นเมื่อมีการเลือกตัวแปรในหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dcc8d-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![ข้อผิดพลาดเมื่อมีการเลือกตัวแปรในหน้ารายละเอียดผลิตภัณฑ์](media/unhandled-rejection-error.jpg)

<span data-ttu-id="dcc8d-114">ภาพต่อไปนี้แสดงตัวอย่างข้อผิดพลาดที่คล้ายกันในเครื่องมือดีบักเกอร์ของเบราเซอร์ (เครื่องมือสำหรับนักพัฒนา F12)</span><span class="sxs-lookup"><span data-stu-id="dcc8d-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="dcc8d-115">ข้อความแสดงข้อผิดพลาดกล่าวถึงการละเมิดตัวควบคุมนโยบายความปลอดภัยของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="dcc8d-115">The error message mentions violation of the content security policy directive.</span></span>

![ข้อผิดพลาดเกี่ยวกับเครื่องมือดีบักเกอร์](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="dcc8d-117">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="dcc8d-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="dcc8d-118">ปิดใช้งานนโยบายความปลอดภัยเนื้อหาของไซต์ของโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="dcc8d-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="dcc8d-119">เลือกไซต์ที่คุณพยายามใช้</span><span class="sxs-lookup"><span data-stu-id="dcc8d-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="dcc8d-120">เลือก **การตั้งค่า** แล้วจากนั้นเลือก **ส่วนขยาย**</span><span class="sxs-lookup"><span data-stu-id="dcc8d-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="dcc8d-121">บนแท็บ **นโยบายความปลอดภัยของเนื้อหา** ให้เลือก **ปิดใช้งานนโยบายความปลอดภัยของเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="dcc8d-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="dcc8d-122">เลือก **Save and publish**</span><span class="sxs-lookup"><span data-stu-id="dcc8d-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="dcc8d-123">การลงชื่อเข้าใช้แบบธุรกิจ-ผู้บริโภค (B2C) จะไม่ทำงานในสภาพแวดล้อมการพัฒนาเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="dcc8d-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="dcc8d-124">อย่างไรก็ตาม คุณสามารถใช้การเช็คเอาท์สำหรับแขกหรือสร้างการจำลองหน้าเพื่อจําลองการลงชื่อเข้าใช้ของผู้ใช้ตามความจําเป็น</span><span class="sxs-lookup"><span data-stu-id="dcc8d-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dcc8d-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dcc8d-125">Additional resources</span></span>

[<span data-ttu-id="dcc8d-126">เริ่มต้นใช้งานการพัฒนาความสามารถในการเพิ่มฟังก์ชันออนไลน์ของอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="dcc8d-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="dcc8d-127">จัดการนโยบายความปลอดภัยของเนื้อหา (CSP) บนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="dcc8d-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
