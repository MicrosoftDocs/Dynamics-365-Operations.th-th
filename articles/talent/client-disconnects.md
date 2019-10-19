---
title: ไคลเอนต์ talent ยกเลิกการเชื่อมต่อ
description: หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าถูกยกเลิกการเชื่อมต่อจากสภาพแวดล้อมของเขาหรือเธอ และไม่รู้ว่าเพราะอะไร
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6d174a8acac3863fb6d9f9431c6bc777cb717470
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008186"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="fa3eb-103">ไคลเอนต์ talent ยกเลิกการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="fa3eb-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa3eb-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="fa3eb-104">**Environment details**</span></span> 

<span data-ttu-id="fa3eb-105">ปัญหานี้อาจเกิดขึ้นในสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fa3eb-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="fa3eb-106">**อาการ**</span><span class="sxs-lookup"><span data-stu-id="fa3eb-106">**Symptom**</span></span> 

<span data-ttu-id="fa3eb-107">ลูกค้าถูกยกเลิกการเชื่อมต่อจากสภาพแวดล้อมของเขาหรือเธอ และไม่รู้ว่าเพราะอะไร</span><span class="sxs-lookup"><span data-stu-id="fa3eb-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="fa3eb-108">ลูกค้าจะได้รับหนึ่งในข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fa3eb-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="fa3eb-109">เราได้เสียการเชื่อมต่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="fa3eb-109">We've lost your connection.</span></span> <span data-ttu-id="fa3eb-110">คลิกปิดเพื่อทำงานต่อไป</span><span class="sxs-lookup"><span data-stu-id="fa3eb-110">Click Close to continue working.</span></span>
- <span data-ttu-id="fa3eb-111">การเชื่อมต่อเครือข่ายของคุณอาจขาดหายไป คลิก ลองอีกครั้ง เพื่อลองใหม่</span><span class="sxs-lookup"><span data-stu-id="fa3eb-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="fa3eb-112">**แฟล็กสีแดง**</span><span class="sxs-lookup"><span data-stu-id="fa3eb-112">**Red flag**</span></span>

<span data-ttu-id="fa3eb-113">ปัญหานี้มักเกิดขึ้น เมื่อผู้ใช้อยู่ในระยะการใช้งาน จะเปรียบเทียบข้อมูลระหว่างการผลิต และสภาพแวดล้อมการทดสอบ และลืมว่ามีการย้ายระหว่างเซสชัน</span><span class="sxs-lookup"><span data-stu-id="fa3eb-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="fa3eb-114">ถ้าผู้ใช้ในขั้นตอนนี้ พวกเขามักจะพบปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="fa3eb-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="fa3eb-115">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="fa3eb-115">**Issue**</span></span> 

<span data-ttu-id="fa3eb-116">**ชนิดเบราว์เซอร์:** Google Chrome Internet Explorer และ Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fa3eb-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="fa3eb-117">Microsoft Dynamics 365 Talent ยกเลิกการเชื่อมต่อผู้ใช้ เมื่อเซสชั่นที่แตกต่างกันสองรายการเปิดขึ้นในเวลาเดียวกันสำหรับผู้ใช้เดียวกันและชนิดเบราว์เซอร์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="fa3eb-117">Microsoft Dynamics 365 Talent disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="fa3eb-118">(ตัวอย่างเช่น ผู้ใช้ A กำลังดูทั้งสภาพแวดล้อมที่ 1 และ 2 สภาพแวดล้อมใน Chrome) ไม่สำคัญว่าผู้ใช้เปิด windows เบราเซอร์อื่นหรือแท็บอื่น</span><span class="sxs-lookup"><span data-stu-id="fa3eb-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="fa3eb-119">ถ้ามีการใช้ข้อมูลประจำตัวผู้ใช้เดียวกันเพื่อลงชื่อเข้าใช้ในทั้งสภาพแวดล้อมที่ 1 และสภาพแวดล้อมที่ 2 พร้อมกัน และในเบราเซอร์ชนิดเดียวกัน Talent จะยกเลิกการเชื่อมต่อหนึ่งในเซสชันเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="fa3eb-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="fa3eb-120">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="fa3eb-120">**Solution**</span></span>

<span data-ttu-id="fa3eb-121">ตรวจสอบว่า สภาพแวดล้อมเดียวเท่านั้นถูกเปิดอยู่ในคราวเดียวสำหรับชนิดของเบราเซอร์ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="fa3eb-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="fa3eb-122">ผู้ใช้สามารถเปิดรอบเวลาหลายรอบไปยังสภาพแวดล้อมเดียวกันได้ (นั่นคือ แท็บหลายแท็บในเบราเซอร์เดียวกัน)</span><span class="sxs-lookup"><span data-stu-id="fa3eb-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="fa3eb-123">ผู้ใช้ที่ต้องการข้ามระหว่างสภาพแวดล้อมสองรายการในเวลาเดียวกัน ควรเปิดสภาพแวดล้อมแต่ละรายการในชนิดเบราเซอร์อื่น</span><span class="sxs-lookup"><span data-stu-id="fa3eb-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="fa3eb-124">(ตัวอย่างเช่น ผู้ใช้ A สามารถดูสภาพแวดล้อม 1 ได้ใน Chrome และสภาพแวดล้อม 2 ใน Microsoft Edge)</span><span class="sxs-lookup"><span data-stu-id="fa3eb-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
