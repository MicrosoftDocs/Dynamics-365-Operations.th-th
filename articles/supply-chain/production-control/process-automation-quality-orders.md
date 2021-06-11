---
title: เรียกขั้นตอนระบบอัตโนมัติของกระบวนการเพื่อสร้างใบสั่งตรวจสอบคุณภาพ
description: หัวข้อนี้มีทรัพยากรในการใช้ Power Automate เพื่อทำกระบวนการทางธุรกิจโดยอัตโนมัติ โดยใช้ตัวอย่างของใบสั่งตรวจสอบคุณภาพ
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115222"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="f6e82-103">เรียกขั้นตอนระบบอัตโนมัติของกระบวนการเพื่อสร้างใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f6e82-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="f6e82-104">องค์กรมีความต้องการที่เพิ่มขึ้นเพื่อปรับกระบวนการทางธุรกิจมาตรฐานโดยอัตโนมัติ ให้การติดต่อของพนักงานที่สะดวกขึ้น และใช้สัญญาณและระบบข้อมูลต่างๆ เพื่อผลักดันกระบวนการทางธุรกิจโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f6e82-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="f6e82-105">ด้วยระบบอัตโนมัติของกระบวนการเฉพาะบริษัท (RPA) และ Microsoft Power Automate ธุรกิจสามารถใช้ประสบการณ์ที่ไม่มีรหัสเพื่อกํากับกับกระบวนการที่ซ้ํากันโดยอัตโนมัติ จึงเพิ่มประสิทธิภาพและความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f6e82-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="f6e82-106">แม่แบบโซลูชันระบบอัตโนมัติที่สามารถดาวน์โหลดได้สำหรับ Supply Chain Management แสดงวิธีการ Power Automate สามารถใช้เพื่อกรับกระบวนการทางธุรกิจโดยอัตโนมัติโดยใช้ใบสั่งตรวจสอบคุณภาพเป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f6e82-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="f6e82-107">คุณสามารถดาวน์โหลดแม่แบบโซลูชันระบบอัตโนมัติ [ที่นี่](https://aka.ms/D365SCMQualityOrderRPASolution)</span><span class="sxs-lookup"><span data-stu-id="f6e82-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="f6e82-108">สำหรับภาพรวมของคุณลักษณะนี้และความสามารถของคุณลักษณะนี้ โปรดดูวิดีโอต่อไปนี้: [ใช้ RPA เพื่อสร้างใบสั่งตรวจสอบคุณภาพใน Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="f6e82-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="f6e82-109">![ตัวเลือกระบบอัตโนมัติที่มี RPA](media/rpa-automation-options.png "ตัวเลือกระบบอัตโนมัติที่มี RPA")</span><span class="sxs-lookup"><span data-stu-id="f6e82-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="f6e82-110">แม่แบบโซลูชัน Power Automate ประกอบด้วยโฟลว์ระบบอัตโนมัติของระบบคลาวด์ และโฟลว์ระบบอัตโนมัติบนเดสก์ทอปที่สร้างใบสั่งตรวจสอบคุณภาพใน Supply Chain Management ปโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f6e82-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="f6e82-111">ระบบอัตโนมัติสามารถเริ่มต้นขึ้นเพื่อตอบสนองต่อเหตุการณ์และสัญญาณต่างๆ รวมทั้งสัญญาณอินพุตของผู้ใช้หรือเครื่อง (รวมทั้ง Internet of Things (IoT))</span><span class="sxs-lookup"><span data-stu-id="f6e82-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="f6e82-112">ตัวอย่าง *Q-Order* Power Application รวมอยู่ในแม่แบบโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="f6e82-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="f6e82-113">ซึ่งช่วยให้ผู้ใช้สามารถสแกนคิวอาร์โค้ดสินค้า ป้อนปริมาณ และแนบรูปภาพโดยใช้กล้องได้</span><span class="sxs-lookup"><span data-stu-id="f6e82-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="f6e82-114">พารามิเตอร์โซลูชันถูกรวมไว้เพื่อตั้งค่าคอนฟิกระบบอัตโนมัติให้กับกรณีการใช้เฉพาะในสิ่งอำนวยความสะดวกในการผลิต</span><span class="sxs-lookup"><span data-stu-id="f6e82-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="f6e82-115">![สร้างใบสั่งตรวจสอบคุณภาพ](media/rpa-create-quality-roder.png "สร้างใบสั่งตรวจสอบคุณภาพ")</span><span class="sxs-lookup"><span data-stu-id="f6e82-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="f6e82-116">สำหรับขั้นตอนทั้งหมดเกี่ยวกับวิธีการดาวน์โหลด ติดตั้ง และใช้โซลูชันตัวอย่างเพื่อการสร้างใบสั่งตรวจสอบคุณภาพอัตโนมัติ โปรดดูที่ [การสร้างใบสั่งตรวจสอบคุณภาพอัตโนมัติบน Dynamics 365 Supply Chain Management ด้วยการดำเนินการอัตโนมัติแบบหุ่นยนต์โดยใช้ Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa)</span><span class="sxs-lookup"><span data-stu-id="f6e82-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

