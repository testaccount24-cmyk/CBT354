# CBT354
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 354 IS FROM RANDY HALL OF VICTORIA, BRITISH COLUMBIA,     *   FILE 354
//*           AND CONTAINS A LARGE COLLECTION OF PROGRAMS WRITTEN   *   FILE 354
//*           BY HIM OR MODIFIED BY HIM.  INCLUDED IS A VERSION     *   FILE 354
//*           OF THE DISASSEMBLER FROM FILE 171, AND A PROGRAM      *   FILE 354
//*           TO MAKE IEBCOPY BACKUPS FROM A LIST OF DATASETS,      *   FILE 354
//*           WHICH IS CALLED BACKDSNS.  THERE ARE OTHER PROGRAMS   *   FILE 354
//*           TOO, LISTED BELOW.                                    *   FILE 354
//*                                                                 *   FILE 354
//*   - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -   *   FILE 354
//*                                                                 *   FILE 354
//*     FEBRUARY 1999. THIS FILE CONTAINS SEVERAL PROGRAMS          *   FILE 354
//*                    CREATED OR MODIFIED BY:                      *   FILE 354
//*                                                                 *   FILE 354
//*      RANDY HALL,                                                *   FILE 354
//*      1151 PALMER ROAD,                                          *   FILE 354
//*      VICTORIA, B.C.                                             *   FILE 354
//*      V8P-2H5                                                    *   FILE 354
//*      PHONE: HOME: 250-385-1061      WORK: 250-413-8229          *   FILE 354
//*      E-MAIL:RANDY.HALL@I.AM         RANDY.HALL@GEMS9.GOV.BC.CA  *   FILE 354
//*             RANDY.HALL@USA.NET                                  *   FILE 354
//*                                                                 *   FILE 354
//*     $$$$$DOC IS THE "MASTER DOC" FOR THIS FILE. THIS FILE       *   FILE 354
//*     CONTAINS SEVERAL DIFFERENT PROGRAMS THAT ARE FURTHER        *   FILE 354
//*     DOCUMENTED IN INDIVIDUAL $$DOC... MEMBERS IF THE            *   FILE 354
//*     INSTALLATION IS MORE COMPLICATED THAN JUST RUNNING THE      *   FILE 354
//*     JOB.                                                        *   FILE 354
//*                                                                 *   FILE 354
//*     IF THERE IS NO $$DOC... MEMBER, THE PROGRAM SHOULD          *   FILE 354
//*     HOPEFULLY BE SELF-CONTAINED AND SELF-EXPLANATORY.           *   FILE 354
//*                                                                 *   FILE 354
//*     JCL IN ALL JOBS WILL HAVE TO BE MODIFIED FOR YOUR           *   FILE 354
//*     DATASET NAMES AND YOUR PROCEDURE NAMES.                     *   FILE 354
//*                                                                 *   FILE 354
//*     ALSO NOTE THAT I'M ONE OF THOSE PROGRAMMERS WHO DOESN'T     *   FILE 354
//*     DELETE CODE...  I JUST COMMENT IT OUT, SO SOME SOURCE       *   FILE 354
//*     MAY HAVE A LOT OF COMMENTED CODE!                           *   FILE 354
//*                                                                 *   FILE 354
//*     A LOT OF THE PROGRAMS IN THIS FILE DO NOT SPECIFICALLY      *   FILE 354
//*     HAVE A COPYRIGHT NOTICE IMBEDDED IN THEM, SO THIS           *   FILE 354
//*     NOTICE APPLIES TO ALL MY SOURCE....                         *   FILE 354
//*                                                                 *   FILE 354
//*                COPYRIGHT                                        *   FILE 354
//*        THE METHODS AND CODE IN THIS PROGRAM ARE COPYRIGHTED     *   FILE 354
//*        BY:                                                      *   FILE 354
//*                                                                 *   FILE 354
//*        RANDY HALL,                                              *   FILE 354
//*        1151 PALMER ROAD,                                        *   FILE 354
//*        VICTORIA, B.C. CANADA, V8P-2H5                           *   FILE 354
//*        E-MAIL...BITRON@ISLANDNET.COM OR RANDY.HALL@I.AM         *   FILE 354
//*                                                                 *   FILE 354
//*        YOU MUST LEAVE IT AS IS, AND CANNOT SELL IT TO ANYONE,   *   FILE 354
//*        OR MODIFY IT, WITHOUT MY  PERMISSION.                    *   FILE 354
//*                                                                 *   FILE 354
//*     IF YOU DO MAKE CHANGES, I WOULD APPRECIATE IT IF YOU        *   FILE 354
//*     SENT ME A COPY SO THAT I CAN KEEP MY SOURCE UP-TO-DATE.     *   FILE 354
//*     THANKS...                                                   *   FILE 354
//*                                                                 *   FILE 354
//*     THE PROGRAMS, AND THEIR INDIVIDUAL "DOC"S ARE:              *   FILE 354
//*                                                                 *   FILE 354
//*     PROGRAM                DESCRIPTION                          *   FILE 354
//*     -------                -----------                          *   FILE 354
//*     ABS.......             MACRO TO SIMULATE THE PLI ABS        *   FILE 354
//*                            FUNCTION - WRITTEN 90/01/03          *   FILE 354
//*                                                                 *   FILE 354
//*     A31BITMD..             EXAMPLE OF 31 BIT MODE AND SEE       *   FILE 354
//*                            IF A MODULE IS LOADED                *   FILE 354
//*                                                                 *   FILE 354
//*     BACKDSNS..             UTILITY TO BACKUP A LIST OF          *   FILE 354
//*                            DATASETS.                            *   FILE 354
//*                            LAST ASSEMBLED 99/01/29              *   FILE 354
//*     BACKSAMP..             SAMPLE JCL TO BACKUP DATASETS.       *   FILE 354
//*     BACKSAM2..             SAMPLE JCL TO RESTORE DATASETS.      *   FILE 354
//*                                                                 *   FILE 354
//*     BLNKSCRN..             SAMPLE CODE TO BLANK A 3270 SCREEN   *   FILE 354
//*                            LAST ASSEMBLED 96/02/02              *   FILE 354
//*                                                                 *   FILE 354
//*     CALLIDC...             HOW TO CALL IDCAMS IN A PROGRAM      *   FILE 354
//*                            LAST ASSEMBLED 99/02/02              *   FILE 354
//*     CALLIDCT..             SAMPLE JCL TO RUN CALLIDC            *   FILE 354
//*                                                                 *   FILE 354
//*     CDSCB.....             TSO COMMAND TO MODIFY DSCB'S.        *   FILE 354
//*                            ORIGINALLY WRITTEN BY BILL GODFREY.  *   FILE 354
//*                            I ADDED RACF SUPPORT FOR CONTROL.    *   FILE 354
//*                            SEE THE COMMENTS IN THE PROGRAM.     *   FILE 354
//*                            LAST ASSEMBLED 98/08/28              *   FILE 354
//*                                                                 *   FILE 354
//*     CHKOTMA...             PROGRAM TO CHECK THAT                *   FILE 354
//*                            TCPIP/IMSOTMA INTERFACE IS           *   FILE 354
//*                            WORKING. THIS REQUIRES A             *   FILE 354
//*                            TRANSACTION CALLED WHOAMI.           *   FILE 354
//*                            LAST ASSEMBLED 98/12/21              *   FILE 354
//*                                                                 *   FILE 354
//*     CHKOTMAR..             REXX EXEC TO INVOKE CHKOTMA.         *   FILE 354
//*                            CHKOTMA AND CHKOTMAR WILL HAVE       *   FILE 354
//*                            TO BE MODIFIED FOR YOUR PORT         *   FILE 354
//*                            NUMBERS, ETC...                      *   FILE 354
//*                                                                 *   FILE 354
//*     DATEFB....             READ A FIXED LENGTH FILE AND         *   FILE 354
//*                            CHANGE THE DATE FIELD TO INCLUDE     *   FILE 354
//*                            THE CENTURY.                         *   FILE 354
//*                            LAST ASSEMBLED 97/02/14              *   FILE 354
//*     DATEFBJ...             SAMPLE JCL TO RUN DATEFB             *   FILE 354
//*                                                                 *   FILE 354
//*     DATEVB....             READ A VARIABLE LENGTH FILE AND      *   FILE 354
//*                            CHANGE THE DATE FIELD TO INCLUDE     *   FILE 354
//*                            THE CENTURY.                         *   FILE 354
//*                            LAST ASSEMBLED 97/02/14              *   FILE 354
//*     DATEVBJ...             SAMPLE JCL TO RUN DATEVB             *   FILE 354
//*                                                                 *   FILE 354
//*     DAYDATE...             TIME OF DAY AND DATE SUBROUTINE.     *   FILE 354
//*                            DAYDATE IS INCLUDED IN IUTDEL        *   FILE 354
//*                            AND JDATE.                           *   FILE 354
//*                            LAST ASSEMBLED 98/01/09              *   FILE 354
//*                                                                 *   FILE 354
//*     DELMEMS...             DELETE LIST OF MEMBERS FROM PDS      *   FILE 354
//*                            LAST ASSEMBLED 91/06/19              *   FILE 354
//*     DELMEMSJ..             SAMPLE JCL TO RUN DELMEMS            *   FILE 354
//*                                                                 *   FILE 354
//*     DISALINK..$$DOCDIS     PROGRAM TO DIS-ASSEMBLE CSECTS       *   FILE 354
//*     DISASM                                                      *   FILE 354
//*     DISASM1                                                     *   FILE 354
//*     DISASM2                                                     *   FILE 354
//*     DISASM3A                                                    *   FILE 354
//*     DISASM3B                                                    *   FILE 354
//*     DISASPRM                                                    *   FILE 354
//*                            LAST ASSEMBLED 99/01/08              *   FILE 354
//*     DISASRUN..             SAMPLE JCL TO RUN DISASM             *   FILE 354
//*                                                                 *   FILE 354
//*     DSPACE....             TSO COMMAND TO DISPLAY DATASET       *   FILE 354
//*                            INFORMATION.                         *   FILE 354
//*                                                                 *   FILE 354
//*     (DS)                   CAN ALSO BE RUN IN BATCH.            *   FILE 354
//*                            LAST ASSEMBLED 99/01/14              *   FILE 354
//*     DSB.......             REXX EXEC TO RUN DS                  *   FILE 354
//*                                                                 *   FILE 354
//*     ENQ.......             THIS VERSION IS FOR PRE-SP3          *   FILE 354
//*                            SYSTEMS COMMAND TO LIST ENQUEUED     *   FILE 354
//*                            DATASET NAMES LAST ASSEMBLED         *   FILE 354
//*                            82/07/16...MAY NEED WORK!            *   FILE 354
//*                                                                 *   FILE 354
//*     FILEDUMP..             A PROGRAM THAT WILL LIST (DUMP)      *   FILE 354
//*                            ANY FILE IN AN ABEND TYPE            *   FILE 354
//*                            LISTING.  SEE HOWFDUMP FOR           *   FILE 354
//*                            DOCUMENTATION.  LAST ASSEMBLED       *   FILE 354
//*                            90/03/13...STILL WORKS.              *   FILE 354
//*                                                                 *   FILE 354
//*     FILEDUMJ..             SAMPLE JCL TO RUN FILEDUMP           *   FILE 354
//*                                                                 *   FILE 354
//*     FREEALL...             TSO COMMAND PROCESSOR USED TO        *   FILE 354
//*                            FREE ALL DYNAMICALLY ALLOCATED       *   FILE 354
//*                            DATA SETS WHICH HAVE BEEN            *   FILE 354
//*                            ALLOCATED BY A TSO USER.             *   FILE 354
//*                            ORIGINALLY FROM CBT320,              *   FILE 354
//*                            10/20/75...                          *   FILE 354
//*                            LAST ASSEMBLED 92/10/28...STILL      *   FILE 354
//*                            WORKS.                               *   FILE 354
//*                                                                 *   FILE 354
//*     GENQ......             COMMAND TO LIST ENQUEUED DATASET     *   FILE 354
//*                            NAMES.  THIS VERSION IS FOR SP3      *   FILE 354
//*                            SYSTEMS                              *   FILE 354
//*                            LAST ASSEMBLED 96/07/11...STILL      *   FILE 354
//*                            WORKS.                               *   FILE 354
//*     GENQCLST..             CLIST TO RUN GENQ                    *   FILE 354
//*                                                                 *   FILE 354
//*     GETDSNS...             GET A LIST OF ALL CATALOGUED         *   FILE 354
//*                            DATASETS FOR HLI IN SYSIN.  CAN BE   *   FILE 354
//*                            USED TO GET DATASET NAMES FOR        *   FILE 354
//*                            BACKDSNS.  LAST ASSEMBLED            *   FILE 354
//*                            95/10/30...STILL WORKS.              *   FILE 354
//*                                                                 *   FILE 354
//*     GETDSNSJ..             SAMPLE JCL TO RUN GETDSNS            *   FILE 354
//*                                                                 *   FILE 354
//*     HALLDUMP..             EXAMPLE OF HOW TO USE HDUMP          *   FILE 354
//*                            LAST ASSEMBLED 98/12/13              *   FILE 354
//*                                                                 *   FILE 354
//*     HDUMP.....             MACRO TO DUMP CORE IN A RUNNING      *   FILE 354
//*                            PROGRAM.                             *   FILE 354
//*                            LAST ASSEMBLED 98/12/13              *   FILE 354
//*                                                                 *   FILE 354
//*     HOWBACK                SCRIPT DOCUMENTATION FOR BACKDSNS    *   FILE 354
//*                                                                 *   FILE 354
//*     HOWDELM                SCRIPT DOCUMENTATION FOR DELMEMS     *   FILE 354
//*                                                                 *   FILE 354
//*     HOWDISAS               DOCUMENTATION FOR DISASM             *   FILE 354
//*                                                                 *   FILE 354
//*     HOWDS                  DOCUMENTATION FOR DS(PACE) FOR       *   FILE 354
//*                            PAPER THERE IS A SYS1.HELP           *   FILE 354
//*                            VERSION WITH THE PROGRAM.            *   FILE 354
//*                                                                 *   FILE 354
//*     HOWFDUMP               DOCUMENTATION FOR FILEDUMP           *   FILE 354
//*                                                                 *   FILE 354
//*     HOWHDUMP               DOCUMENTATION FOR HDUMP              *   FILE 354
//*                                                                 *   FILE 354
//*     HOWSETDT               DOCUMENTATION FOR SETDATE            *   FILE 354
//*                                                                 *   FILE 354
//*     HOWTCOPY               DOCUMENTATION FOR TAPECOPY           *   FILE 354
//*                                                                 *   FILE 354
//*     HOWVSPLT               DOCUMENTATION FOR VSPLIT             *   FILE 354
//*                                                                 *   FILE 354
//*     IUTDEL....             DELETE MEMBERS FROM A PDS WITH       *   FILE 354
//*                            AN AUDIT TRAIL                       *   FILE 354
//*                            LAST ASSEMBLED 91/06/19              *   FILE 354
//*     IUTDELJ...             SAMPLE JCL TO RUN IUTDEL             *   FILE 354
//*                                                                 *   FILE 354
//*     JDATE.....             TSO COMMAND TO DISPLAY TODAYS        *   FILE 354
//*                            JULIAN DATE, ETC.                    *   FILE 354
//*                            LAST ASSEMBLED 97/03/16              *   FILE 354
//*                                                                 *   FILE 354
//*     JOBNAME...             GET JOB NAME AND NUMBER FROM         *   FILE 354
//*                            JES2, COMPARE TO TIOT.               *   FILE 354
//*                            SEE SETDATEC FOR AN EXAMPLE OF       *   FILE 354
//*                            HOW TO USE IT.                       *   FILE 354
//*                            LAST ASSEMBLED 93/12/13              *   FILE 354
//*                                                                 *   FILE 354
//*     LINKDATE.....          PROGRAM TO CREATE LIST OF MEMBER     *   FILE 354
//*                            NAMES AND LINK DATES IN A PDS.       *   FILE 354
//*                            LAST ASSEMBLED 99/01/18              *   FILE 354
//*     LINKDATJ..             SAMPLE JCL TO RUN LINKDATE           *   FILE 354
//*                                                                 *   FILE 354
//*     MEMLIST......          PRODUCE A LIST OF MEMBERS IN         *   FILE 354
//*                            A PDS.                               *   FILE 354
//*                            NAMES ARE IN COLUMNS 1-8             *   FILE 354
//*                            LAST ASSEMBLED 93/10/18              *   FILE 354
//*     MEMLISTJ..             SAMPLE JCL TO RUN MEMLIST            *   FILE 354
//*                                                                 *   FILE 354
//*     MACROS....   MACRO     USED FOR...                          *   FILE 354
//*                  BEGIN     GENERATE ENTRY CODE WITH BASE        *   FILE 354
//*                            REGS R13,&B,&C                       *   FILE 354
//*                  DEBUG     GENERATE CODE  TO PRINT A            *   FILE 354
//*                            CSECT TRACE                          *   FILE 354
//*                  IBMMAC    GENERATE DCB AND JFCB DSECTS         *   FILE 354
//*                  MSGRTN    GENERATE CODE TO PRINT MESSAGES      *   FILE 354
//*                  OLCMSG    GENERATE CODE TO PRINT A MSG         *   FILE 354
//*                  PERFORM   GENERATE CODE TO BRANCH TO A CSECT   *   FILE 354
//*                  REQUATE   GENERATE REGISTER EQUATES, AND       *   FILE 354
//*                            A SAVEAREA DSECT                     *   FILE 354
//*                  SAVESET   GENERATE IMS STYLE SAVE AREAS        *   FILE 354
//*                  SECEXIT   GENERATE CSECT EXIT CODE             *   FILE 354
//*                  SECTION   GENERATE CSECT ENTRY CODE            *   FILE 354
//*                                                                 *   FILE 354
//*     MOD.......             MACRO THAT SIMULATES THE PLI MOD     *   FILE 354
//*                            FUNCTION                             *   FILE 354
//*                                                                 *   FILE 354
//*     PGMDATE......          PRODUCE LIST OF MEMBERS IN A PDS     *   FILE 354
//*                            OLDER THAN SPECIFIED DATE.           *   FILE 354
//*                            LAST ASSEMBLED 99/01/19              *   FILE 354
//*     PGMDATEJ..             SAMPLE JCL TO RUN PGMDATE            *   FILE 354
//*                                                                 *   FILE 354
//*     PRINTDOC               SAMPLE JCL TO PRINT SCRIPT           *   FILE 354
//*                            DOCUMENTATION.  THIS WILL HAVE       *   FILE 354
//*                            TO BE MODIFIED A LOT...              *   FILE 354
//*                                                                 *   FILE 354
//*     SETDATE...             PUT DATE INTO A CONTROL RECORD       *   FILE 354
//*                            IN A DATASET, OR PASS IT BACK IN     *   FILE 354
//*                            THE PARM.                            *   FILE 354
//*                            LAST ASSEMBLED 97/10/30              *   FILE 354
//*     SETDATEC..             SAMPLE PLI PROGRAM CALLING SETDATE   *   FILE 354
//*                            LAST ASSEMBLED 97/08/19              *   FILE 354
//*     SETDATEJ..             SAMPLE JCL CALLING SETDATE           *   FILE 354
//*                                                                 *   FILE 354
//*     SLOCATE...             SAMPLE CODE TO CALL SUPER LOCATE     *   FILE 354
//*                            SEE DSPACE FOR USAGE...              *   FILE 354
//*                                                                 *   FILE 354
//*     SMFEXIT...             THIS LITTLE PROGRAM IS USED TO       *   FILE 354
//*                            PRODUCE A READABLE REPORT BASED      *   FILE 354
//*                            ON TYPE 14, 15, 17 AND 18 SMF        *   FILE 354
//*                            RECORDS                              *   FILE 354
//*                            LAST ASSEMBLED 92/11/17              *   FILE 354
//*                                                                 *   FILE 354
//*     SUBEDIT....            SUBMIT ANY 1-126 BYTE COMMAND FROM   *   FILE 354
//*                            PARM= OR  //SYSIN                    *   FILE 354
//*     SUBEDITJ..             SAMPLE JCL CALLING SUBEDIT           *   FILE 354
//*                                                                 *   FILE 354
//*     TAPECOPY..             A PROGRAM THAT WILL LIST (DUMP)      *   FILE 354
//*                            OR COPY A TAPE.                      *   FILE 354
//*                            SEE HOWTCOPY FOR DOCUMENTATION.      *   FILE 354
//*                            LAST ASSEMBLED 90/03/15.             *   FILE 354
//*     TAPECOPJ..             SAMPLE JCL TO RUN TAPECOPY           *   FILE 354
//*                                                                 *   FILE 354
//*     VSPLIT....             UTILITY PROGRAM TO SELECT            *   FILE 354
//*                            RECORDS FROM A VB FILE.              *   FILE 354
//*                            LAST ASSEMBLED 96/07/03              *   FILE 354
//*     VSPLITJ...             SAMPLE JCL CALLING VSPLIT TO         *   FILE 354
//*                            SELECT SPECIFIC RECORDS FROM AN      *   FILE 354
//*                            IMS LOG                              *   FILE 354
//*                                                                 *   FILE 354
//*     WHOAMI....             IMS TRANSACTION CALLED BY CHKOTMA.   *   FILE 354
//*                            LAST ASSEMBLED 98/11/03              *   FILE 354
//*                                                                 *   FILE 354
//*     YRDOC                  DOCUMENTATION FOR YR2000             *   FILE 354
//*                                                                 *   FILE 354
//*     YR2000....             UTILITY PROGRAM TO DETERMINE IF      *   FILE 354
//*                            LOAD MODULES ACCESS THE SYSTEM       *   FILE 354
//*                            DATE OR A DATE ROUTINE               *   FILE 354
//*                            LAST ASSEMBLED 99/01/27              *   FILE 354
//*     YR2000J...             SAMPLE JCL CALLING YR2000            *   FILE 354
//*                                                                 *   FILE 354
//*     ZELLERS...             ASSEMBLER VERSION OF T.F. WONG'S     *   FILE 354
//*                            CALCULATE DAY OF WEEK FORMULA.       *   FILE 354
//*                            SEE DAYDATE FOR USAGE...             *   FILE 354
//*                                                                 *   FILE 354
//*           SEE http://www/asiaonlin.net.hk/~tfwong/maths.htm     *   FILE 354
//*                    (MAY HAVE TO BE IN LOWER CASE)               *   FILE 354
//*                                                                 *   FILE 354
```
