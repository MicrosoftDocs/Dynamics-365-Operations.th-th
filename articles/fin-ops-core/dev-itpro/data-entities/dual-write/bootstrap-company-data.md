---
title: ปลุกเครื่องด้วยคำถามที่ถามบ่อยเกี่ยวกับข้อมูลของบริษัท
description: วิธีการปลุกเครื่องข้อมูลของ Dataverse หรือแอป Dynamics 365 ด้วยข้อมูลของบริษัทก่อนที่จะเปิดใช้งานการเชื่อมต่อแบบการเขียนแบบสองครั้ง
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 8cd753a5b0d63833a911e0692c83c653e0278153
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683782"
---
# <a name="bootstrap-with-company-data-faq"></a>ปลุกเครื่องด้วยคำถามที่ถามบ่อยเกี่ยวกับข้อมูลของบริษัท
 
[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="why-do-i-need-bootstrapping"></a>เพราะเหตุใดฉันจึงต้องปลุกเครื่อง 
คุณอาจมีอินสแตนซ์ของ Dataverse หรือแอป Dynamics 365 ที่มีอยู่ที่มีข้อมูลธุรกิจ และคุณต้องการเปิดใช้งานการเชื่อมต่อแบบการเขียนแบบสองครั้ง ในกรณีนี้ คุณจำเป็นต้องปลุกเครื่องข้อมูลของ Dataverse หรือแอป Dynamics 365 ด้วยข้อมูลของบริษัทก่อนที่จะเปิดใช้งานการเชื่อมต่อแบบการเขียนแบบสองครั้ง  
 
## <a name="when-should-i-use-bootstrapping"></a>ฉันควรใช้การปลุกเครื่องเมื่อใด 
คุณควรใช้การปลุกเครื่องก่อนที่จะเปิดใช้งานแผนผังตารางการรวมแบบสองทิศทาง (ระหว่างขั้นตอนที่ #5)  
1. เมื่อต้องการตั้งค่าการเชื่อมต่อแบบการเขียนสองครั้งระหว่างอินสแตนซ์ของแอป Finance and Operations และ Dataverse และแอป Dynamics 365 อื่นๆ ให้ล็อกอินไปยังแอป Finance and Operations ในฐานะผู้ดูแลระบบ 
2. ไปที่โมดูล **การจัดการข้อมูล** แล้วคลิกปุ่มแบบ **การเขียนแบบสองครั้ง** ขั้นตอนนี้จะเป็นการเรียกใช้ **ตัวรวมข้อมูล** 
3. สร้างการเชื่อมต่อแบบการเขียนสองครั้งสำหรับบริษัทหนึ่งแห่งขึ้นไป  
    > [!div class="mx-imgBorder"]
    > ![สร้างการเชื่อมต่อแบบการเขียนสองครั้ง](media/dual-write-boot-1.png)
4. เปิดใช้งานแผนผังตาราง **Cdm_companies** นี่จะเป็นการซิงโครไนส์บริษัทจากแอป Finance and Operations ไปยัง Dataverse  
    > [!div class="mx-imgBorder"]
    > ![เปิดใช้งานแผนผังตาราง](media/dual-write-boot-2.png)
5. รันรหัสการปลุกเครื่องตัวอย่างบนอินสแตนซ์ Dataverse หรือแอป Dynamics 365 อื่นๆ  
6. เมื่อปลุกเครื่องเสร็จแล้ว และระบบพร้อมสำหรับการซิงค์สด ให้เปิดใช้งานแผนผังตาราง  

    การเปิดใช้งานแผนผังตารางจะเป็นการทริกเกอร์การซิงค์ข้อมูลเริ่มต้นสำหรับแผนผังตารางที่เปิดใช้งาน ข้อมูลที่เกี่ยวข้องกับบริษัทที่เลือกบนการเชื่อมต่อแบบการเขียนสองครั้งจะถูกซิงโครไนส์ระหว่างแอป Finance and Operations และ Dataverse 
 
## <a name="how-to-i-use-the-code-sample"></a>ฉันจะใช้ตัวอย่างรหัสได้อย่างไร
รหัสตัวอย่างเป็นแอปพลิเคชัน C# ที่คุณสามารถโหลดได้ใน Visual Studio ซึ่งจะใช้การอ้างอิงแพ็คเกจ NuGet บน Dataverse SDK ซึ่งคุณสามารถรีเฟรชผ่านเครื่องมือ Visual Studio มาตรฐาน 

หลังจากที่แตกไฟล์และเปิดโซลูชันใน Visual Studio และคืนค่าแพ็คเกจ NuGet แล้ว ให้ค้นหา **TODO** ในรหัส การตัดสินใจแต่ละครั้งที่คุณต้องทำเกี่ยวกับวิธีการที่คุณต้องการปลุกเครื่องข้อมูลของบริษัทจะถูกจดจำโดย **TODO** ด้วยรหัสตัวอย่างสำหรับการใช้งานที่มีมาตรฐาน 

รหัสตัวอย่างจะแสดงเฉพาะวิธีการใดวิธีการหนึ่งที่คุณสามารถจัดประเภทแถวของเอนทิตีตามบริษัทได้ ด้วยการเปลี่ยนแปลงตรรกะในส่วน **TODO** คุณสามารถสร้างการจัดประเภทที่กำหนดเองของคุณได้ 
 
## <a name="what-should-i-expect"></a>ฉันควรคาดหวังอะไร
โดยค่าเริ่มต้น แอปพลิเคชันตัวอย่างจะช่วยให้คุณสามารถระบุพจนานุกรมของการแม็ปรหัสจากหน่วยธุรกิจไปยังบริษัทได้ เอนทิตีใดๆ ที่คุณปลุกเครื่องด้วยฟิลด์ **OwningBusinessUnit** จะถูกตั้งค่าให้ใช้บริษัทที่ระบุโดยอัตโนมัติ เอนทิตีใดๆ ที่ไม่มีฟิลด์ **OwningBusinessUnit** เช่น ผลิตภัณฑ์ จะตั้งค่าบริษัทตามการแม็ปกับมูลค่าหน่วยธุรกิจที่ว่างเปล่า

แอปพลิเคชันคอนโซลกำหนดให้ต้องมีหนึ่งพารามิเตอร์ ไม่ว่าจะเป็น **–simulate** หรือ **–apply** ถ้าคุณใช้พารามิเตอร์บรรทัดคำสั่ง **–simulate** จะไม่มีการอัพเดตข้อมูล เฉพาะไฟล์ **simulation_<entityname>.csv** เท่านั้นที่จะถูกสร้างขึ้นในไดเรกทอรีเดียวกันกับเครื่องมือ จะมีการอัพเดตหนึ่งไฟล์สำหรับแต่ละเอนทิตี คุณสามารถตรวจทานไฟล์เหล่านี้ซ้ำได้ในขณะที่ทำงานเพื่อให้แน่ใจว่ารหัสจะอัพเดตค่าบริษัทตามที่คาดไว้ 

เมื่อคุณอัพเดตที่จำลองขึ้นเสร็จแล้ว ให้ใช้พารามิเตอร์ **–apply** การทำเช่นนี้จะเป็นการอัปเดตแถวทั้งหมดที่มีค่าของบริษัทที่ไม่ถูกต้อง ในชุดงาน 1000 แถวในแต่ละครั้ง (โดยค่าเริ่มต้น) รหัสจะเหมือนตามที่ระบุ ซึ่งหมายความว่าคุณสามารถรันใหม่ได้และจะมีการอัพเดตเฉพาะบริษัทที่กำหนดอย่างไม่ถูกต้องเท่านั้น เมื่อรันโดยใช้ **–apply** รหัสจะแสดงผลลัพธ์การเปลี่ยนแปลงที่เกิดขึ้นเป็นไฟล์ CSV ซึ่งมีชื่อ **applied_<entityname>.csv** 

 ```csharp
 using Microsoft.Crm.Sdk.Messages;
using Microsoft.Xrm.Sdk;
using Microsoft.Xrm.Sdk.Messages;
using Microsoft.Xrm.Sdk.Query;
using Microsoft.Xrm.Tooling.Connector;
using System;
using System.Collections.Generic;
using System.Diagnostics;
using System.IO;

namespace BootstrapCompany
{
    /// <summary>
    /// Application to bootstrap the company field on existing rows in CDS in preparation for integration to Finance and Operations.
    /// </summary>
    /// <remarks>
    /// This application assumes that the target companies already exist in the CDS environment in the cdm_Company table and are
    /// identified by their company code. It also assumes that the current owning business unit of each row should be used
    /// to categorize by company. This logic can easily be updated to utilize alternate sources of categorization including
    /// custom tables, teams, custom fields on tables, or any other data. This code is provided only as a sample. 
    /// 
    /// To utilize this code, update each of the locations currently denoted with a TODO statement.
    /// 
    /// This code is provided AS IS with no warranties or guarantees, and confers no rights.
    /// </remarks>
    public class Program
    {
        /// <summary>
        /// The number of rows to query and update in CDS in a single operation.
        /// </summary>
        /// <remarks>
        /// The larger this number, the fewer calls will need to be made, so the faster the updates
        /// will complete. However, larger batch sizes are more likely to cause contention. Additionally,
        /// when SQL exceeds some threshold of locks (generally around 5,000), it will escalate to
        /// an entire table lock, which blocks all other activity in the live system on this table. As 
        /// such, a batch size of around 1,000 is relatively fast, while also relatively safe in terms
        /// of contention and transaction time.
        /// </remarks>
        const int requestBatchSize = 1000;

        /// <summary>
        /// The number of faults that may be seen in CDS before the operation is aborted and an exception is thrown.
        /// </summary>
        /// <remarks>
        /// An occassional error due to contention when updating large tables in production is expected, so by default
        /// errors are logged and skipped. However, if a large number of errors are seen, ignoring those errors
        /// in subsequent batches gets expensive, and is usually indicative of a larger issue that should be addressed
        /// before continuing. Faulted requests are *not* retried, but would be picked up in a subsequent run of this script.
        /// </remarks>
        const int maxFaultThreshold = 100;

        /// <summary>
        /// The maximum number of rows per business unit to export when simulating.
        /// </summary>
        /// <remarks>
        /// During simulation, queries are not batched since doing so would require ordering and so be slightly
        /// different from the actual execution logic. To keep this the same between both paths, simulates are
        /// not batched and so a separate maximum number of rows per business unit can be specified.
        /// </remarks>
        const int maxSimulateRecordsPerBusinessUnit = 10000;

        /// <summary>
        /// Whether or not operations should continue if any errors are encountered.
        /// </summary>
        /// <remarks>
        /// This is different than setting maxFaultThreshold = 0, since the first batch of updates will be processed
        /// together. If continueOnError is true and maxFaultThreshold is 0, it is possible that multiple errors may
        /// be encountered and at the same time some rows successfully updated. In a healthy system when updating
        /// a higher number of rows, an occasional spurious error is expected, so it is recommended this be left as true.
        /// </remarks>
        const bool continueOnError = true;

        #region private variables
        private static Dictionary<string, EntityReference> cachedCompanyReferences = new Dictionary<string, EntityReference>();
        #endregion

        /// <summary>
        /// The main execution loop of the program.
        /// </summary>
        /// <param name="args">No arguments are expected.</param>
        static void Main(string[] args)
        {
            if (args.Length != 1 && args[0] != "-simulate" && args[0] != "-apply")
            {
                Console.WriteLine("Usage: BootstrapCompany -simulate");
                Console.WriteLine("       BootstrapCompany -apply");
                Console.WriteLine("The -simulate flag will create a file called simulation.csv in the working");
                Console.WriteLine("directory, but will not change any data. The -apply flag will update live data");
                Console.WriteLine("in the same way that was demonstrated in the simulation.");

                return;
            }

            bool isSimulate = args[0].Equals("-simulate", StringComparison.OrdinalIgnoreCase);

            // Delete the simulation or applied files if existing
            foreach (string existingSimulate in Directory.EnumerateFiles(Directory.GetCurrentDirectory(), $"{(isSimulate ? "simulation" : "applied")}_*.csv"))
            {
                File.Delete(existingSimulate);
            }

            IOrganizationService orgService;

            // TODO: Provide your connection string details for your environment
            CrmServiceClient cdsConnection = new CrmServiceClient("AuthType=Office365;Username=youraliashere@yourdomainhere.com;Password=yourpasswordhere;URL=https://yourorganizationurlhere.crm.dynamics.com/;");
            orgService = (IOrganizationService)cdsConnection.OrganizationWebProxyClient != null ? (IOrganizationService)cdsConnection.OrganizationWebProxyClient : (IOrganizationService)cdsConnection.OrganizationServiceProxy;

            if (orgService != null)
            {
                // Get the current user ID to verify the connection was successful
                Guid userid = ((WhoAmIResponse)orgService.Execute(new WhoAmIRequest())).UserId;

                if (userid != Guid.Empty)
                {
                    Console.WriteLine("Connection Successful!");
                }

                // TODO: Provide a mapping of OwningBusinessUnit name to cdm_Company company ID. You can reuse
                // the same company ID for multiple business units if desired. In this example, it assumes that
                // the business unit named "USMF" is related to the company "USMF". If all rows were owned
                // by the same root business unit, then the first field in the dictionary should be set to the 
                // name of the root business unit, usually the same value as the organization (eg, "Contoso").
                Dictionary<string, string> businessUnitToCompanyMapping = new Dictionary<string, string>()
                {
                    { "", "USMF" }, // The default mapping to use for any entity that doesn't have an owningbusinessunit field
                    { "USMF", "USMF" },
                    { "FRRT", "FRRT" },
                };

                // TODO: Provide a list of tables for which the company field should be backfilled based
                // on owning business unit. The list below represents all existing tables for which a cdm_Company
                // lookup field was added as part of the Finance and Operations dual write project.
                BatchUpdateEntity(orgService, "account", "msdyn_company", businessUnitToCompanyMapping, true, isSimulate, "accountnumber", "name");
                BatchUpdateEntity(orgService, "contact", "msdyn_company", businessUnitToCompanyMapping, true, isSimulate, "fullname");
                // ... Add more here

                // Note, the product entity does not have an owningbusinessunit field like most other tables, so
                // assigning company by Business Unit is not applicable. In this case, whichever mapping specifies an
                // empty business unit will be used to categorize tables without an owningbusinessunit field.
                BatchUpdateEntity(orgService, "product", "msdyn_companyid", businessUnitToCompanyMapping, false, isSimulate, "productnumber");
            }
            else
            {
                Console.WriteLine("Connection failed...");
            }

            Console.WriteLine("Done");
            Console.ReadLine();
        }

        /// <summary>
        /// Updates all incorrectly assigned company relationships for the specified entity.
        /// </summary>
        /// <param name="orgService">The connection to CDS.</param>
        /// <param name="entityName">The logical name of the entity to update.</param>
        /// <param name="companyFieldName">The physical name of the field in the entity being updated which contains the cdm_Company id.</param>
        /// <param name="businessUnitToCompanyMapping">A dictionary of business unit name to company code.</param>
        /// <param name="hasOwningBusinessUnit">true if the entity has an owningbusinessunit field; otherwise, false.</param>
        /// <param name="isSimulate">true to simulate output; otherwise, false.</param>
        /// <param name="fieldsToExport">A set of fields to export into a CSV for this entity if simulating.</param>
        /// <returns>true if the entity was successfully processed without any errors; otherwise, false.</returns>
        private static bool BatchUpdateEntity(
            IOrganizationService orgService, 
            string entityName, 
            string companyFieldName, 
            Dictionary<string, string> businessUnitToCompanyMapping, 
            bool hasOwningBusinessUnit, 
            bool isSimulate, 
            params string[] fieldsToExport)
        {
            List<Guid> faultedIds = new List<Guid>();
            int totalRecordsProcessed = 0;
            Stopwatch stopwatch = new Stopwatch();
            stopwatch.Start();

            string fileName = isSimulate ? "simulation" : "applied";
            StreamWriter simulationWriter = new StreamWriter(Path.Combine(Directory.GetCurrentDirectory(), $"{fileName}_{entityName}.csv"), true);
            simulationWriter.Write("EntityName,EntityId,");
            foreach (string fieldToExport in fieldsToExport)
            {
                simulationWriter.Write($"{fieldToExport},");
            }
            simulationWriter.WriteLine("BusinessUnit,NewCompanyId");

            // Process each mapped business unit individually
            foreach (string businessUnitName in businessUnitToCompanyMapping.Keys)
            {
                Console.WriteLine("Updating any {0} rows for business unit {1} to company {2}...", entityName, businessUnitName, businessUnitToCompanyMapping[businessUnitName]);

                // The empty business unit value is only applicable for tables without an owning business unit field
                if (hasOwningBusinessUnit && string.IsNullOrEmpty(businessUnitName))
                {
                    continue;
                }
                else if (!hasOwningBusinessUnit && !string.IsNullOrEmpty(businessUnitName))
                {
                    continue;
                }

                var companyRef = GetCompanyReference(orgService, businessUnitToCompanyMapping[businessUnitName]);

                // Iteratively loop in batches to keep transaction lock size small
                bool moreRecordsExist = true;

                while (moreRecordsExist)
                {
                    moreRecordsExist = false;

                    // Find the first batch of rows for this business unit with the wrong company ID. Ordering
                    // is not explicity specified, but SQL will most likely process based on the index starting with
                    // company ID, since all new company ID fields added for Finance and Operations integration have
                    // also added a new index starting with company ID. Explicitly specifying order would reduce the
                    // query plan options for SQL and introduce unnecessary overhead.
                    QueryExpression query = new QueryExpression(entityName);
                    query.ColumnSet.AddColumns(companyFieldName);
                    foreach (string fieldToExport in fieldsToExport)
                    {
                        query.ColumnSet.AddColumn(fieldToExport);
                    }
                    query.Criteria.AddCondition(companyFieldName, ConditionOperator.NotEqual, companyRef.Id);

                    // TODO: Uncomment the line below if you only want to fill in companies that are empty
                    // as opposed to the line above which updates the company any time it differs from the 
                    // desired value
                    // query.Criteria.AddCondition(companyFieldName, ConditionOperator.Equal, Guid.Empty);

                    if (isSimulate)
                    {
                        // During simulation, get as a single block of rows to avoid positioning complexities
                        query.TopCount = maxSimulateRecordsPerBusinessUnit;
                    }
                    else
                    {
                        // Only batch rows during actual application, otherwise retrieve all as a single operation
                        query.TopCount = requestBatchSize + faultedIds.Count;
                    }

                    // For tables with an owning business unit, join based on business unit name
                    if (hasOwningBusinessUnit)
                    {
                        // TODO: Replace this logic with different algorithms to determine the correct company
                        // in situations where business unit is not the best way to categorize.
                        LinkEntity linkEntity = query.AddLink("businessunit", "owningbusinessunit", "businessunitid", JoinOperator.Inner);
                        linkEntity.Columns.AddColumns("name");
                        linkEntity.LinkCriteria.AddCondition("name", ConditionOperator.Equal, businessUnitName);
                    }

                    var multipleRequest = new ExecuteMultipleRequest()
                    {
                        Settings = new ExecuteMultipleSettings()
                        {
                            ContinueOnError = true,
                            ReturnResponses = true
                        },
                        Requests = new OrganizationRequestCollection()
                    };

                    EntityCollection result = orgService.RetrieveMultiple(query);

                    int rowsAddedToBatch = 0;

                    foreach (var entity in result.Entities)
                    {
                        // Skip any previously faulted ID's. These values will be re-queried with each batch
                        // which is inefficient, but is more efficient than passing hundreds of ID values to 
                        // the underlying SQL query to be skipped at the database level (assuming the 
                        // max fault count is relatively small).
                        if (faultedIds.Contains(entity.Id))
                        {
                            continue;
                        }

                        entity.Attributes[companyFieldName] = companyRef;
                        
                        UpdateRequest updateRequest = new UpdateRequest()
                        {
                            Target = entity
                        };

                        simulationWriter.Write($"{entityName},{entity.Id},");
                        foreach (string fieldToExport in fieldsToExport)
                        {
                            simulationWriter.Write($"{entity.Attributes[fieldToExport]},");
                        }
                        simulationWriter.WriteLine($"{businessUnitName},{businessUnitToCompanyMapping[businessUnitName]}");

                        // Only add the update request when applying for real
                        if (!isSimulate)
                        {
                            multipleRequest.Requests.Add(updateRequest);
                        }

                        rowsAddedToBatch++;
                        Console.Write(".");
                    }

                    totalRecordsProcessed += rowsAddedToBatch;

                    if (rowsAddedToBatch > 0 && !isSimulate)
                    {
                        Console.Write("Sending {0} updates in a batch", rowsAddedToBatch);
                        var updateResult = orgService.Execute(multipleRequest) as ExecuteMultipleResponse;
                        moreRecordsExist = true;
                        Console.WriteLine(" done");

                        // If any faults are encountered, flag those IDs to not be processed again
                        // in subsequent batches.
                        if (updateResult.IsFaulted)
                        {
                            foreach (var response in updateResult.Responses)
                            {
                                if (response.Fault != null)
                                {
                                    Console.WriteLine(response.Fault);
                                    faultedIds.Add(((UpdateRequest)multipleRequest.Requests[response.RequestIndex]).Target.Id);

                                    if (faultedIds.Count > 100)
                                    {
                                        throw new ApplicationException("Excessive number of update failures, aborting operation");
                                    }
                                }
                            }
                        }
                    }
                    else
                    {
                        Console.WriteLine("No {0} rows remain to be updated for {1}->{2}", entityName, businessUnitName, businessUnitToCompanyMapping[businessUnitName]);
                    }
                }
            }

            simulationWriter.Close();
            simulationWriter = null;

            stopwatch.Stop();
            Console.WriteLine("Processed {0} rows for the {1} entity in {2}ms.", totalRecordsProcessed, entityName, stopwatch.ElapsedMilliseconds);

            return (faultedIds.Count == 0);
        }

        /// <summary>
        /// Gets an entity reference to the company with the specified ID if one exists.
        /// </summary>
        /// <param name="orgService">The CDS connection.</param>
        /// <param name="companyId">The company ID to search for.</param>
        /// <returns>An entity reference if one exists; otherwise, null.</returns>
        private static EntityReference GetCompanyReference(IOrganizationService orgService, string companyId)
        {
            if (cachedCompanyReferences.ContainsKey(companyId))
            {
                return cachedCompanyReferences[companyId];
            }

            QueryExpression query = new QueryExpression("cdm_company");
            query.ColumnSet.AddColumns("cdm_companyid");
            query.Criteria.AddCondition("cdm_companycode", ConditionOperator.Equal, companyId);
            query.TopCount = 1;

            EntityCollection result = orgService.RetrieveMultiple(query);

            EntityReference entityRef = null;

            foreach (var entity in result.Entities)
            {
                entityRef = entity.ToEntityReference();
                break;
            }

            cachedCompanyReferences[companyId] = entityRef;

            return entityRef;
        }
    }
}

 ```
 
 
