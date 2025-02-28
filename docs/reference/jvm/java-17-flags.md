# Reference: Java 17 JVM flags

A complete list of all flags available for the JVM, created using the `-XX:+PrintFlagsFinal` option and the results written to a file

```bash
java -XX:+PrintFlagsFinal > java-flags.md
```

Find specific flags by using grep on the output with a name

```shell
java -XX:+PrintFlagsFinal -version | grep MaxHeap
```

| Type   | Name             | Units      | ?            | ?           |
|--------|------------------|------------|--------------|-------------|
| uintx  | MaxHeapFreeRatio | 70         | {manageable} | {default}   |
| size_t | MaxHeapSize      | 8342470656 | {product}    | {ergonomic} |
| size_t | SoftMaxHeapSize  | 8342470656 | {manageable} | {ergonomic} |

## Full list of JVM flags

| Type      | Option Name                                      |        Default value | Product                | Category       |
|:----------|:-------------------------------------------------|---------------------:|:-----------------------|:---------------|
| int       | ActiveProcessorCount                             |                   -1 | {product}              | {default}      |
| uintx     | AdaptiveSizeDecrementScaleFactor                 |                    4 | {product}              | {default}      |
| uintx     | AdaptiveSizeMajorGCDecayTimeScale                |                   10 | {product}              | {default}      |
| uintx     | AdaptiveSizePolicyCollectionCostMargin           |                   50 | {product}              | {default}      |
| uintx     | AdaptiveSizePolicyInitializingSteps              |                   20 | {product}              | {default}      |
| uintx     | AdaptiveSizePolicyOutputInterval                 |                    0 | {product}              | {default}      |
| uintx     | AdaptiveSizePolicyWeight                         |                   10 | {product}              | {default}      |
| uintx     | AdaptiveSizeThroughPutPolicy                     |                    0 | {product}              | {default}      |
| uintx     | AdaptiveTimeWeight                               |                   25 | {product}              | {default}      |
| bool      | AdjustStackSizeForTLS                            |                false | {product}              | {default}      |
| bool      | AggressiveHeap                                   |                false | {product}              | {default}      |
| intx      | AliasLevel                                       |                    3 | {C2 product}           | {default}      |
| bool      | AlignVector                                      |                false | {C2 product}           | {default}      |
| ccstr     | AllocateHeapAt                                   |                      | {product}              | {default}      |
| intx      | AllocateInstancePrefetchLines                    |                    1 | {product}              | {default}      |
| intx      | AllocatePrefetchDistance                         |                  256 | {product}              | {default}      |
| intx      | AllocatePrefetchInstr                            |                    0 | {product}              | {default}      |
| intx      | AllocatePrefetchLines                            |                    3 | {product}              | {default}      |
| intx      | AllocatePrefetchStepSize                         |                   64 | {product}              | {default}      |
| intx      | AllocatePrefetchStyle                            |                    1 | {product}              | {default}      |
| bool      | AllowParallelDefineClass                         |                false | {product}              | {default}      |
| bool      | AllowRedefinitionToAddDeleteMethods              |                false | {product}              | {default}      |
| bool      | AllowUserSignalHandlers                          |                false | {product}              | {default}      |
| bool      | AllowVectorizeOnDemand                           |                 true | {C2 product}           | {default}      |
| bool      | AlwaysActAsServerClassMachine                    |                false | {product}              | {default}      |
| bool      | AlwaysCompileLoopMethods                         |                false | {product}              | {default}      |
| bool      | AlwaysLockClassLoader                            |                false | {product}              | {default}      |
| bool      | AlwaysPreTouch                                   |                false | {product}              | {default}      |
| bool      | AlwaysRestoreFPU                                 |                false | {product}              | {default}      |
| bool      | AlwaysTenure                                     |                false | {product}              | {default}      |
| ccstr     | ArchiveClassesAtExit                             |                      | {product}              | {default}      |
| intx      | ArrayCopyLoadStoreMaxElem                        |                    8 | {C2 product}           | {default}      |
| size_t    | AsyncLogBufferSize                               |              2097152 | {product}              | {default}      |
| intx      | AutoBoxCacheMax                                  |                  128 | {C2 product}           | {default}      |
| intx      | BCEATraceLevel                                   |                    0 | {product}              | {default}      |
| bool      | BackgroundCompilation                            |                 true | {pd product}           | {default}      |
| size_t    | BaseFootPrintEstimate                            |            268435456 | {product}              | {default}      |
| intx      | BiasedLockingBulkRebiasThreshold                 |                   20 | {product}              | {default}      |
| intx      | BiasedLockingBulkRevokeThreshold                 |                   40 | {product}              | {default}      |
| intx      | BiasedLockingDecayTime                           |                25000 | {product}              | {default}      |
| intx      | BiasedLockingStartupDelay                        |                    0 | {product}              | {default}      |
| bool      | BlockLayoutByFrequency                           |                 true | {C2 product}           | {default}      |
| intx      | BlockLayoutMinDiamondPercentage                  |                   20 | {C2 product}           | {default}      |
| bool      | BlockLayoutRotateLoops                           |                 true | {C2 product}           | {default}      |
| intx      | C1InlineStackLimit                               |                    5 | {C1 product}           | {default}      |
| intx      | C1MaxInlineLevel                                 |                    9 | {C1 product}           | {default}      |
| intx      | C1MaxInlineSize                                  |                   35 | {C1 product}           | {default}      |
| intx      | C1MaxRecursiveInlineLevel                        |                    1 | {C1 product}           | {default}      |
| intx      | C1MaxTrivialSize                                 |                    6 | {C1 product}           | {default}      |
| bool      | C1OptimizeVirtualCallProfiling                   |                 true | {C1 product}           | {default}      |
| bool      | C1ProfileBranches                                |                 true | {C1 product}           | {default}      |
| bool      | C1ProfileCalls                                   |                 true | {C1 product}           | {default}      |
| bool      | C1ProfileCheckcasts                              |                 true | {C1 product}           | {default}      |
| bool      | C1ProfileInlinedCalls                            |                 true | {C1 product}           | {default}      |
| bool      | C1ProfileVirtualCalls                            |                 true | {C1 product}           | {default}      |
| bool      | C1UpdateMethodData                               |                 true | {C1 product}           | {default}      |
| intx      | CICompilerCount                                  |                   12 | {product}              | {ergonomic}    |
| bool      | CICompilerCountPerCPU                            |                 true | {product}              | {default}      |
| bool      | CITime                                           |                false | {product}              | {default}      |
| bool      | CheckJNICalls                                    |                false | {product}              | {default}      |
| bool      | ClassUnloading                                   |                 true | {product}              | {default}      |
| bool      | ClassUnloadingWithConcurrentMark                 |                 true | {product}              | {default}      |
| bool      | ClipInlining                                     |                 true | {product}              | {default}      |
| uintx     | CodeCacheExpansionSize                           |                65536 | {pd product}           | {default}      |
| bool      | CompactStrings                                   |                 true | {pd product}           | {default}      |
| ccstr     | CompilationMode                                  |              default | {product}              | {default}      |
| ccstrlist | CompileCommand                                   |                      | {product}              | {default}      |
| ccstr     | CompileCommandFile                               |                      | {product}              | {default}      |
| ccstrlist | CompileOnly                                      |                      | {product}              | {default}      |
| intx      | CompileThreshold                                 |                10000 | {pd product}           | {default}      |
| double    | CompileThresholdScaling                          |             1.000000 | {product}              | {default}      |
| intx      | CompilerThreadPriority                           |                   -1 | {product}              | {default}      |
| intx      | CompilerThreadStackSize                          |                 1024 | {pd product}           | {default}      |
| size_t    | CompressedClassSpaceSize                         |           1073741824 | {product}              | {default}      |
| uint      | ConcGCThreads                                    |                    3 | {product}              | {ergonomic}    |
| intx      | ConditionalMoveLimit                             |                    3 | {C2 pd product}        | {default}      |
| intx      | ContendedPaddingWidth                            |                  128 | {product}              | {default}      |
| bool      | CrashOnOutOfMemoryError                          |                false | {product}              | {default}      |
| bool      | CreateCoredumpOnCrash                            |                 true | {product}              | {default}      |
| bool      | CriticalJNINatives                               |                false | {product}              | {default}      |
| bool      | DTraceAllocProbes                                |                false | {product}              | {default}      |
| bool      | DTraceMethodProbes                               |                false | {product}              | {default}      |
| bool      | DTraceMonitorProbes                              |                false | {product}              | {default}      |
| bool      | DisableAttachMechanism                           |                false | {product}              | {default}      |
| bool      | DisableExplicitGC                                |                false | {product}              | {default}      |
| bool      | DisplayVMOutputToStderr                          |                false | {product}              | {default}      |
| bool      | DisplayVMOutputToStdout                          |                false | {product}              | {default}      |
| bool      | DoEscapeAnalysis                                 |                 true | {C2 product}           | {default}      |
| bool      | DoReserveCopyInSuperWord                         |                 true | {C2 product}           | {default}      |
| bool      | DontCompileHugeMethods                           |                 true | {product}              | {default}      |
| bool      | DontYieldALot                                    |                false | {pd product}           | {default}      |
| ccstr     | DumpLoadedClassList                              |                      | {product}              | {default}      |
| bool      | DumpReplayDataOnError                            |                 true | {product}              | {default}      |
| bool      | DumpSharedSpaces                                 |                false | {product}              | {default}      |
| bool      | DynamicDumpSharedSpaces                          |                false | {product}              | {default}      |
| bool      | EagerXrunInit                                    |                false | {product}              | {default}      |
| intx      | EliminateAllocationArraySizeLimit                |                   64 | {C2 product}           | {default}      |
| bool      | EliminateAllocations                             |                 true | {C2 product}           | {default}      |
| bool      | EliminateAutoBox                                 |                 true | {C2 product}           | {default}      |
| bool      | EliminateLocks                                   |                 true | {C2 product}           | {default}      |
| bool      | EliminateNestedLocks                             |                 true | {C2 product}           | {default}      |
| bool      | EnableContended                                  |                 true | {product}              | {default}      |
| bool      | EnableDynamicAgentLoading                        |                 true | {product}              | {default}      |
| size_t    | ErgoHeapSizeLimit                                |                    0 | {product}              | {default}      |
| ccstr     | ErrorFile                                        |                      | {product}              | {default}      |
| bool      | ErrorFileToStderr                                |                false | {product}              | {default}      |
| bool      | ErrorFileToStdout                                |                false | {product}              | {default}      |
| uint64_t  | ErrorLogTimeout                                  |                  120 | {product}              | {default}      |
| double    | EscapeAnalysisTimeout                            |            20.000000 | {C2 product}           | {default}      |
| bool      | EstimateArgEscape                                |                 true | {product}              | {default}      |
| bool      | ExecutingUnitTests                               |                false | {product}              | {default}      |
| bool      | ExitOnOutOfMemoryError                           |                false | {product}              | {default}      |
| bool      | ExplicitGCInvokesConcurrent                      |                false | {product}              | {default}      |
| bool      | ExtendedDTraceProbes                             |                false | {product}              | {default}      |
| bool      | ExtensiveErrorReports                            |                false | {product}              | {default}      |
| ccstr     | ExtraSharedClassListFile                         |                      | {product}              | {default}      |
| bool      | FilterSpuriousWakeups                            |                 true | {product}              | {default}      |
| bool      | FlightRecorder                                   |                false | {product}              | {default}      |
| ccstr     | FlightRecorderOptions                            |                      | {product}              | {default}      |
| bool      | ForceTimeHighResolution                          |                false | {product}              | {default}      |
| intx      | FreqInlineSize                                   |                  325 | {C2 pd product}        | {default}      |
| double    | G1ConcMarkStepDurationMillis                     |            10.000000 | {product}              | {default}      |
| uintx     | G1ConcRSHotCardLimit                             |                    4 | {product}              | {default}      |
| size_t    | G1ConcRSLogCacheSize                             |                   10 | {product}              | {default}      |
| size_t    | G1ConcRefinementGreenZone                        |                    0 | {product}              | {default}      |
| size_t    | G1ConcRefinementRedZone                          |                    0 | {product}              | {default}      |
| uintx     | G1ConcRefinementServiceIntervalMillis            |                  300 | {product}              | {default}      |
| uint      | G1ConcRefinementThreads                          |                   13 | {product}              | {ergonomic}    |
| size_t    | G1ConcRefinementThresholdStep                    |                    2 | {product}              | {default}      |
| size_t    | G1ConcRefinementYellowZone                       |                    0 | {product}              | {default}      |
| uintx     | G1ConfidencePercent                              |                   50 | {product}              | {default}      |
| size_t    | G1HeapRegionSize                                 |              4194304 | {product}              | {ergonomic}    |
| uintx     | G1HeapWastePercent                               |                    5 | {product}              | {default}      |
| uintx     | G1MixedGCCountTarget                             |                    8 | {product}              | {default}      |
| uintx     | G1PeriodicGCInterval                             |                    0 | {manageable}           | {default}      |
| bool      | G1PeriodicGCInvokesConcurrent                    |                 true | {product}              | {default}      |
| double    | G1PeriodicGCSystemLoadThreshold                  |             0.000000 | {manageable}           | {default}      |
| intx      | G1RSetRegionEntries                              |                  768 | {product}              | {default}      |
| intx      | G1RSetSparseRegionEntries                        |                   32 | {product}              | {default}      |
| intx      | G1RSetUpdatingPauseTimePercent                   |                   10 | {product}              | {default}      |
| uint      | G1RefProcDrainInterval                           |                 1000 | {product}              | {default}      |
| uintx     | G1ReservePercent                                 |                   10 | {product}              | {default}      |
| uintx     | G1SATBBufferEnqueueingThresholdPercent           |                   60 | {product}              | {default}      |
| size_t    | G1SATBBufferSize                                 |                 1024 | {product}              | {default}      |
| size_t    | G1UpdateBufferSize                               |                  256 | {product}              | {default}      |
| bool      | G1UseAdaptiveConcRefinement                      |                 true | {product}              | {default}      |
| bool      | G1UseAdaptiveIHOP                                |                 true | {product}              | {default}      |
| uintx     | GCDrainStackTargetSize                           |                   64 | {product}              | {ergonomic}    |
| uintx     | GCHeapFreeLimit                                  |                    2 | {product}              | {default}      |
| uintx     | GCLockerEdenExpansionPercent                     |                    5 | {product}              | {default}      |
| uintx     | GCPauseIntervalMillis                            |                  201 | {product}              | {default}      |
| uintx     | GCTimeLimit                                      |                   98 | {product}              | {default}      |
| uintx     | GCTimeRatio                                      |                   12 | {product}              | {default}      |
| size_t    | HeapBaseMinAddress                               |           2147483648 | {pd product}           | {default}      |
| bool      | HeapDumpAfterFullGC                              |                false | {manageable}           | {default}      |
| bool      | HeapDumpBeforeFullGC                             |                false | {manageable}           | {default}      |
| intx      | HeapDumpGzipLevel                                |                    0 | {manageable}           | {default}      |
| bool      | HeapDumpOnOutOfMemoryError                       |                false | {manageable}           | {default}      |
| ccstr     | HeapDumpPath                                     |                      | {manageable}           | {default}      |
| uintx     | HeapFirstMaximumCompactionCount                  |                    3 | {product}              | {default}      |
| uintx     | HeapMaximumCompactionInterval                    |                   20 | {product}              | {default}      |
| uintx     | HeapSearchSteps                                  |                    3 | {product}              | {default}      |
| size_t    | HeapSizePerGCThread                              |             43620760 | {product}              | {default}      |
| bool      | IgnoreEmptyClassPaths                            |                false | {product}              | {default}      |
| bool      | IgnoreUnrecognizedVMOptions                      |                false | {product}              | {default}      |
| uintx     | IncreaseFirstTierCompileThresholdAt              |                   50 | {product}              | {default}      |
| bool      | IncrementalInline                                |                 true | {C2 product}           | {default}      |
| uintx     | InitialCodeCacheSize                             |              2555904 | {pd product}           | {default}      |
| size_t    | InitialHeapSize                                  |            490733568 | {product}              | {ergonomic}    |
| uintx     | InitialRAMFraction                               |                   64 | {product}              | {default}      |
| double    | InitialRAMPercentage                             |             1.562500 | {product}              | {default}      |
| uintx     | InitialSurvivorRatio                             |                    8 | {product}              | {default}      |
| uintx     | InitialTenuringThreshold                         |                    7 | {product}              | {default}      |
| uintx     | InitiatingHeapOccupancyPercent                   |                   45 | {product}              | {default}      |
| bool      | Inline                                           |                 true | {product}              | {default}      |
| ccstr     | InlineDataFile                                   |                      | {product}              | {default}      |
| intx      | InlineSmallCode                                  |                 2500 | {C2 pd product}        | {default}      |
| bool      | InlineSynchronizedMethods                        |                 true | {C1 product}           | {default}      |
| intx      | InteriorEntryAlignment                           |                   16 | {C2 pd product}        | {default}      |
| intx      | InterpreterProfilePercentage                     |                   33 | {product}              | {default}      |
| bool      | JavaMonitorsInStackTrace                         |                 true | {product}              | {default}      |
| intx      | JavaPriority10_To_OSPriority                     |                   -1 | {product}              | {default}      |
| intx      | JavaPriority1_To_OSPriority                      |                   -1 | {product}              | {default}      |
| intx      | JavaPriority2_To_OSPriority                      |                   -1 | {product}              | {default}      |
| intx      | JavaPriority3_To_OSPriority                      |                   -1 | {product}              | {default}      |
| intx      | JavaPriority4_To_OSPriority                      |                   -1 | {product}              | {default}      |
| intx      | JavaPriority5_To_OSPriority                      |                   -1 | {product}              | {default}      |
| intx      | JavaPriority6_To_OSPriority                      |                   -1 | {product}              | {default}      |
| intx      | JavaPriority7_To_OSPriority                      |                   -1 | {product}              | {default}      |
| intx      | JavaPriority8_To_OSPriority                      |                   -1 | {product}              | {default}      |
| intx      | JavaPriority9_To_OSPriority                      |                   -1 | {product}              | {default}      |
| size_t    | LargePageHeapSizeThreshold                       |            134217728 | {product}              | {default}      |
| size_t    | LargePageSizeInBytes                             |                    0 | {product}              | {default}      |
| intx      | LiveNodeCountInliningCutoff                      |                40000 | {C2 product}           | {default}      |
| bool      | LoadExecStackDllInVMThread                       |                 true | {product}              | {default}      |
| intx      | LoopMaxUnroll                                    |                   16 | {C2 product}           | {default}      |
| intx      | LoopOptsCount                                    |                   43 | {C2 product}           | {default}      |
| intx      | LoopPercentProfileLimit                          |                   30 | {C2 pd product}        | {default}      |
| uintx     | LoopStripMiningIter                              |                 1000 | {C2 product}           | {default}      |
| uintx     | LoopStripMiningIterShortLoop                     |                  100 | {C2 product}           | {default}      |
| intx      | LoopUnrollLimit                                  |                   60 | {C2 pd product}        | {default}      |
| intx      | LoopUnrollMin                                    |                    4 | {C2 product}           | {default}      |
| bool      | LoopUnswitching                                  |                 true | {C2 product}           | {default}      |
| bool      | ManagementServer                                 |                false | {product}              | {default}      |
| size_t    | MarkStackSize                                    |              4194304 | {product}              | {ergonomic}    |
| size_t    | MarkStackSizeMax                                 |            536870912 | {product}              | {default}      |
| uint      | MarkSweepAlwaysCompactCount                      |                    4 | {product}              | {default}      |
| uintx     | MarkSweepDeadRatio                               |                    5 | {product}              | {default}      |
| intx      | MaxBCEAEstimateLevel                             |                    5 | {product}              | {default}      |
| intx      | MaxBCEAEstimateSize                              |                  150 | {product}              | {default}      |
| uint64_t  | MaxDirectMemorySize                              |                    0 | {product}              | {default}      |
| bool      | MaxFDLimit                                       |                 true | {product}              | {default}      |
| uintx     | MaxGCMinorPauseMillis                            | 18446744073709551615 | {product}              | {default}      |
| uintx     | MaxGCPauseMillis                                 |                  200 | {product}              | {default}      |
| uintx     | MaxHeapFreeRatio                                 |                   70 | {manageable}           | {default}      |
| size_t    | MaxHeapSize                                      |           7818182656 | {product}              | {ergonomic}    |
| intx      | MaxInlineLevel                                   |                   15 | {C2 product}           | {default}      |
| intx      | MaxInlineSize                                    |                   35 | {C2 product}           | {default}      |
| intx      | MaxJNILocalCapacity                              |                65536 | {product}              | {default}      |
| intx      | MaxJavaStackTraceDepth                           |                 1024 | {product}              | {default}      |
| intx      | MaxJumpTableSize                                 |                65000 | {C2 product}           | {default}      |
| intx      | MaxJumpTableSparseness                           |                    5 | {C2 product}           | {default}      |
| intx      | MaxLabelRootDepth                                |                 1100 | {C2 product}           | {default}      |
| intx      | MaxLoopPad                                       |                   15 | {C2 product}           | {default}      |
| size_t    | MaxMetaspaceExpansion                            |              5439488 | {product}              | {default}      |
| uintx     | MaxMetaspaceFreeRatio                            |                   70 | {product}              | {default}      |
| size_t    | MaxMetaspaceSize                                 | 18446744073709551615 | {product}              | {default}      |
| size_t    | MaxNewSize                                       |           4689231872 | {product}              | {ergonomic}    |
| intx      | MaxNodeLimit                                     |                80000 | {C2 product}           | {default}      |
| uint64_t  | MaxRAM                                           |         137438953472 | {pd product}           | {default}      |
| uintx     | MaxRAMFraction                                   |                    4 | {product}              | {default}      |
| double    | MaxRAMPercentage                                 |            25.000000 | {product}              | {default}      |
| intx      | MaxRecursiveInlineLevel                          |                    1 | {C2 product}           | {default}      |
| uintx     | MaxTenuringThreshold                             |                   15 | {product}              | {default}      |
| intx      | MaxTrivialSize                                   |                    6 | {C2 product}           | {default}      |
| intx      | MaxVectorSize                                    |                   32 | {C2 product}           | {default}      |
| ccstr     | MetaspaceReclaimPolicy                           |             balanced | {product}              | {default}      |
| size_t    | MetaspaceSize                                    |             22020096 | {product}              | {default}      |
| bool      | MethodFlushing                                   |                 true | {product}              | {default}      |
| size_t    | MinHeapDeltaBytes                                |              4194304 | {product}              | {ergonomic}    |
| uintx     | MinHeapFreeRatio                                 |                   40 | {manageable}           | {default}      |
| size_t    | MinHeapSize                                      |              8388608 | {product}              | {ergonomic}    |
| intx      | MinInliningThreshold                             |                  250 | {product}              | {default}      |
| intx      | MinJumpTableSize                                 |                   10 | {C2 pd product}        | {default}      |
| size_t    | MinMetaspaceExpansion                            |               327680 | {product}              | {default}      |
| uintx     | MinMetaspaceFreeRatio                            |                   40 | {product}              | {default}      |
| uintx     | MinRAMFraction                                   |                    2 | {product}              | {default}      |
| double    | MinRAMPercentage                                 |            50.000000 | {product}              | {default}      |
| uintx     | MinSurvivorRatio                                 |                    3 | {product}              | {default}      |
| size_t    | MinTLABSize                                      |                 2048 | {product}              | {default}      |
| intx      | MultiArrayExpandLimit                            |                    6 | {C2 product}           | {default}      |
| uintx     | NUMAChunkResizeWeight                            |                   20 | {product}              | {default}      |
| size_t    | NUMAInterleaveGranularity                        |              2097152 | {product}              | {default}      |
| uintx     | NUMAPageScanRate                                 |                  256 | {product}              | {default}      |
| size_t    | NUMASpaceResizeRate                              |           1073741824 | {product}              | {default}      |
| bool      | NUMAStats                                        |                false | {product}              | {default}      |
| ccstr     | NativeMemoryTracking                             |                  off | {product}              | {default}      |
| bool      | NeverActAsServerClassMachine                     |                false | {pd product}           | {default}      |
| bool      | NeverTenure                                      |                false | {product}              | {default}      |
| uintx     | NewRatio                                         |                    2 | {product}              | {default}      |
| size_t    | NewSize                                          |              1363144 | {product}              | {default}      |
| size_t    | NewSizeThreadIncrease                            |                 5320 | {pd product}           | {default}      |
| intx      | NmethodSweepActivity                             |                   10 | {product}              | {default}      |
| intx      | NodeLimitFudgeFactor                             |                 2000 | {C2 product}           | {default}      |
| uintx     | NonNMethodCodeHeapSize                           |              7602480 | {pd product}           | {ergonomic}    |
| uintx     | NonProfiledCodeHeapSize                          |            122027880 | {pd product}           | {ergonomic}    |
| intx      | NumberOfLoopInstrToAlign                         |                    4 | {C2 product}           | {default}      |
| intx      | ObjectAlignmentInBytes                           |                    8 | {product lp64_product} | {default}      |
| size_t    | OldPLABSize                                      |                 1024 | {product}              | {default}      |
| size_t    | OldSize                                          |              5452592 | {product}              | {default}      |
| bool      | OmitStackTraceInFastThrow                        |                 true | {product}              | {default}      |
| ccstrlist | OnError                                          |                      | {product}              | {default}      |
| ccstrlist | OnOutOfMemoryError                               |                      | {product}              | {default}      |
| intx      | OnStackReplacePercentage                         |                  140 | {pd product}           | {default}      |
| bool      | OptimizeFill                                     |                false | {C2 product}           | {default}      |
| bool      | OptimizePtrCompare                               |                 true | {C2 product}           | {default}      |
| bool      | OptimizeStringConcat                             |                 true | {C2 product}           | {default}      |
| bool      | OptoBundling                                     |                false | {C2 pd product}        | {default}      |
| intx      | OptoLoopAlignment                                |                   16 | {pd product}           | {default}      |
| bool      | OptoRegScheduling                                |                 true | {C2 pd product}        | {default}      |
| bool      | OptoScheduling                                   |                false | {C2 pd product}        | {default}      |
| uintx     | PLABWeight                                       |                   75 | {product}              | {default}      |
| bool      | PSChunkLargeArrays                               |                 true | {product}              | {default}      |
| int       | ParGCArrayScanChunk                              |                   50 | {product}              | {default}      |
| uintx     | ParallelGCBufferWastePct                         |                   10 | {product}              | {default}      |
| uint      | ParallelGCThreads                                |                   13 | {product}              | {default}      |
| size_t    | ParallelOldDeadWoodLimiterMean                   |                   50 | {product}              | {default}      |
| size_t    | ParallelOldDeadWoodLimiterStdDev                 |                   80 | {product}              | {default}      |
| bool      | ParallelRefProcBalancingEnabled                  |                 true | {product}              | {default}      |
| bool      | ParallelRefProcEnabled                           |                 true | {product}              | {default}      |
| bool      | PartialPeelAtUnsignedTests                       |                 true | {C2 product}           | {default}      |
| bool      | PartialPeelLoop                                  |                 true | {C2 product}           | {default}      |
| intx      | PartialPeelNewPhiDelta                           |                    0 | {C2 product}           | {default}      |
| uintx     | PausePadding                                     |                    1 | {product}              | {default}      |
| intx      | PerBytecodeRecompilationCutoff                   |                  200 | {product}              | {default}      |
| intx      | PerBytecodeTrapLimit                             |                    4 | {product}              | {default}      |
| intx      | PerMethodRecompilationCutoff                     |                  400 | {product}              | {default}      |
| intx      | PerMethodTrapLimit                               |                  100 | {product}              | {default}      |
| bool      | PerfAllowAtExitRegistration                      |                false | {product}              | {default}      |
| bool      | PerfBypassFileSystemCheck                        |                false | {product}              | {default}      |
| intx      | PerfDataMemorySize                               |                32768 | {product}              | {default}      |
| intx      | PerfDataSamplingInterval                         |                   50 | {product}              | {default}      |
| ccstr     | PerfDataSaveFile                                 |                      | {product}              | {default}      |
| bool      | PerfDataSaveToFile                               |                false | {product}              | {default}      |
| bool      | PerfDisableSharedMem                             |                false | {product}              | {default}      |
| intx      | PerfMaxStringConstLength                         |                 1024 | {product}              | {default}      |
| size_t    | PreTouchParallelChunkSize                        |              4194304 | {pd product}           | {default}      |
| bool      | PreferContainerQuotaForCPUCount                  |                 true | {product}              | {default}      |
| bool      | PreferInterpreterNativeStubs                     |                false | {pd product}           | {default}      |
| intx      | PrefetchCopyIntervalInBytes                      |                  576 | {product}              | {default}      |
| intx      | PrefetchFieldsAhead                              |                    1 | {product}              | {default}      |
| intx      | PrefetchScanIntervalInBytes                      |                  576 | {product}              | {default}      |
| bool      | PreserveAllAnnotations                           |                false | {product}              | {default}      |
| bool      | PreserveFramePointer                             |                false | {pd product}           | {default}      |
| size_t    | PretenureSizeThreshold                           |                    0 | {product}              | {default}      |
| bool      | PrintClassHistogram                              |                false | {manageable}           | {default}      |
| bool      | PrintCodeCache                                   |                false | {product}              | {default}      |
| bool      | PrintCodeCacheOnCompilation                      |                false | {product}              | {default}      |
| bool      | PrintCommandLineFlags                            |                false | {product}              | {default}      |
| bool      | PrintCompilation                                 |                false | {product}              | {default}      |
| bool      | PrintConcurrentLocks                             |                false | {manageable}           | {default}      |
| bool      | PrintExtendedThreadInfo                          |                false | {product}              | {default}      |
| bool      | PrintFlagsFinal                                  |                 true | {product}              | {command line} |
| bool      | PrintFlagsInitial                                |                false | {product}              | {default}      |
| bool      | PrintFlagsRanges                                 |                false | {product}              | {default}      |
| bool      | PrintGC                                          |                false | {product}              | {default}      |
| bool      | PrintGCDetails                                   |                false | {product}              | {default}      |
| bool      | PrintHeapAtSIGBREAK                              |                 true | {product}              | {default}      |
| bool      | PrintSharedArchiveAndExit                        |                false | {product}              | {default}      |
| bool      | PrintSharedDictionary                            |                false | {product}              | {default}      |
| bool      | PrintStringTableStatistics                       |                false | {product}              | {default}      |
| bool      | PrintTieredEvents                                |                false | {product}              | {default}      |
| bool      | PrintVMOptions                                   |                false | {product}              | {default}      |
| bool      | PrintWarnings                                    |                 true | {product}              | {default}      |
| uintx     | ProcessDistributionStride                        |                    4 | {product}              | {default}      |
| bool      | ProfileInterpreter                               |                 true | {pd product}           | {default}      |
| intx      | ProfileMaturityPercentage                        |                   20 | {product}              | {default}      |
| uintx     | ProfiledCodeHeapSize                             |            122027880 | {pd product}           | {ergonomic}    |
| uintx     | PromotedPadding                                  |                    3 | {product}              | {default}      |
| uintx     | QueuedAllocationWarningCount                     |                    0 | {product}              | {default}      |
| int       | RTMRetryCount                                    |                    5 | {ARCH product}         | {default}      |
| bool      | RangeCheckElimination                            |                 true | {product}              | {default}      |
| bool      | ReassociateInvariants                            |                 true | {C2 product}           | {default}      |
| bool      | RecordDynamicDumpInfo                            |                false | {product}              | {default}      |
| bool      | ReduceBulkZeroing                                |                 true | {C2 product}           | {default}      |
| bool      | ReduceFieldZeroing                               |                 true | {C2 product}           | {default}      |
| bool      | ReduceInitialCardMarks                           |                 true | {C2 product}           | {default}      |
| bool      | ReduceSignalUsage                                |                false | {product}              | {default}      |
| intx      | RefDiscoveryPolicy                               |                    0 | {product}              | {default}      |
| bool      | RegisterFinalizersAtInit                         |                 true | {product}              | {default}      |
| bool      | RelaxAccessControlCheck                          |                false | {product}              | {default}      |
| ccstr     | ReplayDataFile                                   |                      | {product}              | {default}      |
| bool      | RequireSharedSpaces                              |                false | {product}              | {default}      |
| uintx     | ReservedCodeCacheSize                            |            251658240 | {pd product}           | {ergonomic}    |
| bool      | ResizePLAB                                       |                 true | {product}              | {default}      |
| bool      | ResizeTLAB                                       |                 true | {product}              | {default}      |
| bool      | RestoreMXCSROnJNICalls                           |                false | {product}              | {default}      |
| bool      | RestrictContended                                |                 true | {product}              | {default}      |
| bool      | RestrictReservedStack                            |                 true | {product}              | {default}      |
| bool      | RewriteBytecodes                                 |                 true | {pd product}           | {default}      |
| bool      | RewriteFrequentPairs                             |                 true | {pd product}           | {default}      |
| bool      | SafepointTimeout                                 |                false | {product}              | {default}      |
| intx      | SafepointTimeoutDelay                            |                10000 | {product}              | {default}      |
| bool      | ScavengeBeforeFullGC                             |                false | {product}              | {default}      |
| bool      | SegmentedCodeCache                               |                 true | {product}              | {ergonomic}    |
| intx      | SelfDestructTimer                                |                    0 | {product}              | {default}      |
| ccstr     | SharedArchiveConfigFile                          |                      | {product}              | {default}      |
| ccstr     | SharedArchiveFile                                |                      | {product}              | {default}      |
| size_t    | SharedBaseAddress                                |          34359738368 | {product}              | {default}      |
| ccstr     | SharedClassListFile                              |                      | {product}              | {default}      |
| uintx     | SharedSymbolTableBucketSize                      |                    4 | {product}              | {default}      |
| ccstr     | ShenandoahGCHeuristics                           |             adaptive | {product}              | {default}      |
| ccstr     | ShenandoahGCMode                                 |                 satb | {product}              | {default}      |
| bool      | ShowCodeDetailsInExceptionMessages               |                 true | {manageable}           | {default}      |
| bool      | ShowMessageBoxOnError                            |                false | {product}              | {default}      |
| bool      | ShrinkHeapInSteps                                |                 true | {product}              | {default}      |
| size_t    | SoftMaxHeapSize                                  |           7818182656 | {manageable}           | {ergonomic}    |
| intx      | SoftRefLRUPolicyMSPerMB                          |                 1000 | {product}              | {default}      |
| bool      | SplitIfBlocks                                    |                 true | {C2 product}           | {default}      |
| intx      | StackRedPages                                    |                    1 | {pd product}           | {default}      |
| intx      | StackReservedPages                               |                    1 | {pd product}           | {default}      |
| intx      | StackShadowPages                                 |                   20 | {pd product}           | {default}      |
| bool      | StackTraceInThrowable                            |                 true | {product}              | {default}      |
| intx      | StackYellowPages                                 |                    2 | {pd product}           | {default}      |
| uintx     | StartAggressiveSweepingAt                        |                   10 | {product}              | {default}      |
| bool      | StartAttachListener                              |                false | {product}              | {default}      |
| ccstr     | StartFlightRecording                             |                      | {product}              | {default}      |
| uint      | StringDeduplicationAgeThreshold                  |                    3 | {product}              | {default}      |
| uintx     | StringTableSize                                  |                65536 | {product}              | {default}      |
| bool      | SuperWordLoopUnrollAnalysis                      |                 true | {C2 pd product}        | {default}      |
| bool      | SuperWordReductions                              |                 true | {C2 product}           | {default}      |
| bool      | SuppressFatalErrorMessage                        |                false | {product}              | {default}      |
| uintx     | SurvivorPadding                                  |                    3 | {product}              | {default}      |
| uintx     | SurvivorRatio                                    |                    8 | {product}              | {default}      |
| double    | SweeperThreshold                                 |             0.500000 | {product}              | {default}      |
| uintx     | TLABAllocationWeight                             |                   35 | {product}              | {default}      |
| uintx     | TLABRefillWasteFraction                          |                   64 | {product}              | {default}      |
| size_t    | TLABSize                                         |                    0 | {product}              | {default}      |
| bool      | TLABStats                                        |                 true | {product}              | {default}      |
| uintx     | TLABWasteIncrement                               |                    4 | {product}              | {default}      |
| uintx     | TLABWasteTargetPercent                           |                    1 | {product}              | {default}      |
| uintx     | TargetPLABWastePct                               |                   10 | {product}              | {default}      |
| uintx     | TargetSurvivorRatio                              |                   50 | {product}              | {default}      |
| uintx     | TenuredGenerationSizeIncrement                   |                   20 | {product}              | {default}      |
| uintx     | TenuredGenerationSizeSupplement                  |                   80 | {product}              | {default}      |
| uintx     | TenuredGenerationSizeSupplementDecay             |                    2 | {product}              | {default}      |
| intx      | ThreadPriorityPolicy                             |                    0 | {product}              | {default}      |
| bool      | ThreadPriorityVerbose                            |                false | {product}              | {default}      |
| intx      | ThreadStackSize                                  |                 1024 | {pd product}           | {default}      |
| uintx     | ThresholdTolerance                               |                   10 | {product}              | {default}      |
| intx      | Tier0BackedgeNotifyFreqLog                       |                   10 | {product}              | {default}      |
| intx      | Tier0InvokeNotifyFreqLog                         |                    7 | {product}              | {default}      |
| intx      | Tier0ProfilingStartPercentage                    |                  200 | {product}              | {default}      |
| intx      | Tier23InlineeNotifyFreqLog                       |                   20 | {product}              | {default}      |
| intx      | Tier2BackEdgeThreshold                           |                    0 | {product}              | {default}      |
| intx      | Tier2BackedgeNotifyFreqLog                       |                   14 | {product}              | {default}      |
| intx      | Tier2CompileThreshold                            |                    0 | {product}              | {default}      |
| intx      | Tier2InvokeNotifyFreqLog                         |                   11 | {product}              | {default}      |
| intx      | Tier3BackEdgeThreshold                           |                60000 | {product}              | {default}      |
| intx      | Tier3BackedgeNotifyFreqLog                       |                   13 | {product}              | {default}      |
| intx      | Tier3CompileThreshold                            |                 2000 | {product}              | {default}      |
| intx      | Tier3DelayOff                                    |                    2 | {product}              | {default}      |
| intx      | Tier3DelayOn                                     |                    5 | {product}              | {default}      |
| intx      | Tier3InvocationThreshold                         |                  200 | {product}              | {default}      |
| intx      | Tier3InvokeNotifyFreqLog                         |                   10 | {product}              | {default}      |
| intx      | Tier3LoadFeedback                                |                    5 | {product}              | {default}      |
| intx      | Tier3MinInvocationThreshold                      |                  100 | {product}              | {default}      |
| intx      | Tier4BackEdgeThreshold                           |                40000 | {product}              | {default}      |
| intx      | Tier4CompileThreshold                            |                15000 | {product}              | {default}      |
| intx      | Tier4InvocationThreshold                         |                 5000 | {product}              | {default}      |
| intx      | Tier4LoadFeedback                                |                    3 | {product}              | {default}      |
| intx      | Tier4MinInvocationThreshold                      |                  600 | {product}              | {default}      |
| bool      | TieredCompilation                                |                 true | {pd product}           | {default}      |
| intx      | TieredCompileTaskTimeout                         |                   50 | {product}              | {default}      |
| intx      | TieredRateUpdateMaxTime                          |                   25 | {product}              | {default}      |
| intx      | TieredRateUpdateMinTime                          |                    1 | {product}              | {default}      |
| intx      | TieredStopAtLevel                                |                    4 | {product}              | {default}      |
| bool      | TimeLinearScan                                   |                false | {C1 product}           | {default}      |
| ccstr     | TraceJVMTI                                       |                      | {product}              | {default}      |
| intx      | TrackedInitializationLimit                       |                   50 | {C2 product}           | {default}      |
| bool      | TrapBasedNullChecks                              |                false | {pd product}           | {default}      |
| bool      | TrapBasedRangeChecks                             |                false | {C2 pd product}        | {default}      |
| intx      | TypeProfileArgsLimit                             |                    2 | {product}              | {default}      |
| uintx     | TypeProfileLevel                                 |                  111 | {pd product}           | {default}      |
| intx      | TypeProfileMajorReceiverPercent                  |                   90 | {C2 product}           | {default}      |
| intx      | TypeProfileParmsLimit                            |                    2 | {product}              | {default}      |
| intx      | TypeProfileWidth                                 |                    2 | {product}              | {default}      |
| intx      | UnguardOnExecutionViolation                      |                    0 | {product}              | {default}      |
| bool      | UseAES                                           |                 true | {product}              | {default}      |
| intx      | UseAVX                                           |                    2 | {ARCH product}         | {default}      |
| bool      | UseAdaptiveGenerationSizePolicyAtMajorCollection |                 true | {product}              | {default}      |
| bool      | UseAdaptiveGenerationSizePolicyAtMinorCollection |                 true | {product}              | {default}      |
| bool      | UseAdaptiveNUMAChunkSizing                       |                 true | {product}              | {default}      |
| bool      | UseAdaptiveSizeDecayMajorGCCost                  |                 true | {product}              | {default}      |
| bool      | UseAdaptiveSizePolicy                            |                 true | {product}              | {default}      |
| bool      | UseAdaptiveSizePolicyFootprintGoal               |                 true | {product}              | {default}      |
| bool      | UseAdaptiveSizePolicyWithSystemGC                |                false | {product}              | {default}      |
| bool      | UseAddressNop                                    |                 true | {ARCH product}         | {default}      |
| bool      | UseBASE64Intrinsics                              |                false | {product}              | {default}      |
| bool      | UseBMI1Instructions                              |                 true | {ARCH product}         | {default}      |
| bool      | UseBMI2Instructions                              |                 true | {ARCH product}         | {default}      |
| bool      | UseBiasedLocking                                 |                false | {product}              | {default}      |
| bool      | UseBimorphicInlining                             |                 true | {C2 product}           | {default}      |
| bool      | UseCLMUL                                         |                 true | {ARCH product}         | {default}      |
| bool      | UseCMoveUnconditionally                          |                false | {C2 product}           | {default}      |
| bool      | UseCodeAging                                     |                 true | {product}              | {default}      |
| bool      | UseCodeCacheFlushing                             |                 true | {product}              | {default}      |
| bool      | UseCompiler                                      |                 true | {product}              | {default}      |
| bool      | UseCompressedClassPointers                       |                 true | {product lp64_product} | {ergonomic}    |
| bool      | UseCompressedOops                                |                 true | {product lp64_product} | {ergonomic}    |
| bool      | UseCondCardMark                                  |                false | {product}              | {default}      |
| bool      | UseContainerSupport                              |                 true | {product}              | {default}      |
| bool      | UseCountLeadingZerosInstruction                  |                 true | {ARCH product}         | {default}      |
| bool      | UseCountTrailingZerosInstruction                 |                 true | {ARCH product}         | {default}      |
| bool      | UseCountedLoopSafepoints                         |                 true | {C2 product}           | {default}      |
| bool      | UseCounterDecay                                  |                 true | {product}              | {default}      |
| bool      | UseDivMod                                        |                 true | {C2 product}           | {default}      |
| bool      | UseDynamicNumberOfCompilerThreads                |                 true | {product}              | {default}      |
| bool      | UseDynamicNumberOfGCThreads                      |                 true | {product}              | {default}      |
| bool      | UseEmptySlotsInSupers                            |                 true | {product}              | {default}      |
| bool      | UseFMA                                           |                 true | {product}              | {default}      |
| bool      | UseFPUForSpilling                                |                 true | {C2 product}           | {default}      |
| bool      | UseFastJNIAccessors                              |                 true | {product}              | {default}      |
| bool      | UseFastStosb                                     |                false | {ARCH product}         | {default}      |
| bool      | UseG1GC                                          |                 true | {product}              | {ergonomic}    |
| bool      | UseGCOverheadLimit                               |                 true | {product}              | {default}      |
| bool      | UseHeavyMonitors                                 |                false | {product}              | {default}      |
| bool      | UseHugeTLBFS                                     |                false | {product}              | {default}      |
| bool      | UseInlineCaches                                  |                 true | {product}              | {default}      |
| bool      | UseInterpreter                                   |                 true | {product}              | {default}      |
| bool      | UseJumpTables                                    |                 true | {C2 product}           | {default}      |
| bool      | UseLargePages                                    |                false | {pd product}           | {default}      |
| bool      | UseLargePagesIndividualAllocation                |                false | {pd product}           | {default}      |
| bool      | UseLinuxPosixThreadCPUClocks                     |                 true | {product}              | {default}      |
| bool      | UseLoopCounter                                   |                 true | {product}              | {default}      |
| bool      | UseLoopInvariantCodeMotion                       |                 true | {C1 product}           | {default}      |
| bool      | UseLoopPredicate                                 |                 true | {C2 product}           | {default}      |
| bool      | UseMaximumCompactionOnSystemGC                   |                 true | {product}              | {default}      |
| bool      | UseNUMA                                          |                false | {product}              | {default}      |
| bool      | UseNUMAInterleaving                              |                false | {product}              | {default}      |
| bool      | UseNewLongLShift                                 |                 true | {ARCH product}         | {default}      |
| bool      | UseNotificationThread                            |                 true | {product}              | {default}      |
| bool      | UseOnStackReplacement                            |                 true | {pd product}           | {default}      |
| bool      | UseOnlyInlinedBimorphic                          |                 true | {C2 product}           | {default}      |
| bool      | UseOprofile                                      |                false | {product}              | {default}      |
| bool      | UseOptoBiasInlining                              |                false | {C2 product}           | {default}      |
| bool      | UsePSAdaptiveSurvivorSizePolicy                  |                 true | {product}              | {default}      |
| bool      | UseParallelGC                                    |                false | {product}              | {default}      |
| bool      | UsePerfData                                      |                 true | {product}              | {default}      |
| bool      | UsePopCountInstruction                           |                 true | {product}              | {default}      |
| bool      | UseProfiledLoopPredicate                         |                 true | {C2 product}           | {default}      |
| bool      | UseRTMDeopt                                      |                false | {ARCH product}         | {default}      |
| bool      | UseRTMLocking                                    |                false | {ARCH product}         | {default}      |
| bool      | UseSHA                                           |                 true | {product}              | {default}      |
| bool      | UseSHM                                           |                false | {product}              | {default}      |
| intx      | UseSSE                                           |                    4 | {ARCH product}         | {default}      |
| bool      | UseSSE42Intrinsics                               |                 true | {ARCH product}         | {default}      |
| bool      | UseSerialGC                                      |                false | {product}              | {default}      |
| bool      | UseSharedSpaces                                  |                 true | {product}              | {default}      |
| bool      | UseShenandoahGC                                  |                false | {product}              | {default}      |
| bool      | UseSignalChaining                                |                 true | {product}              | {default}      |
| bool      | UseStoreImmI16                                   |                 true | {ARCH product}         | {default}      |
| bool      | UseStringDeduplication                           |                false | {product}              | {default}      |
| bool      | UseSubwordForMaxVector                           |                 true | {C2 product}           | {default}      |
| bool      | UseSuperWord                                     |                 true | {C2 product}           | {default}      |
| bool      | UseTLAB                                          |                 true | {product}              | {default}      |
| bool      | UseThreadPriorities                              |                 true | {pd product}           | {default}      |
| bool      | UseTransparentHugePages                          |                false | {product}              | {default}      |
| bool      | UseTypeProfile                                   |                 true | {product}              | {default}      |
| bool      | UseTypeSpeculation                               |                 true | {C2 product}           | {default}      |
| bool      | UseUnalignedLoadStores                           |                 true | {ARCH product}         | {default}      |
| bool      | UseVectorCmov                                    |                false | {C2 product}           | {default}      |
| bool      | UseXMMForArrayCopy                               |                 true | {product}              | {default}      |
| bool      | UseXMMForObjInit                                 |                 true | {ARCH product}         | {default}      |
| bool      | UseXmmI2D                                        |                 true | {ARCH product}         | {default}      |
| bool      | UseXmmI2F                                        |                 true | {ARCH product}         | {default}      |
| bool      | UseXmmLoadAndClearUpper                          |                 true | {ARCH product}         | {default}      |
| bool      | UseXmmRegToRegMoveAll                            |                 true | {ARCH product}         | {default}      |
| bool      | UseZGC                                           |                false | {product}              | {default}      |
| intx      | VMThreadPriority                                 |                   -1 | {product}              | {default}      |
| intx      | VMThreadStackSize                                |                 1024 | {pd product}           | {default}      |
| intx      | ValueMapInitialSize                              |                   11 | {C1 product}           | {default}      |
| intx      | ValueMapMaxLoopSize                              |                    8 | {C1 product}           | {default}      |
| intx      | ValueSearchLimit                                 |                 1000 | {C2 product}           | {default}      |
| bool      | VerifySharedSpaces                               |                false | {product}              | {default}      |
| uintx     | YoungGenerationSizeIncrement                     |                   20 | {product}              | {default}      |
| uintx     | YoungGenerationSizeSupplement                    |                   80 | {product}              | {default}      |
| uintx     | YoungGenerationSizeSupplementDecay               |                    8 | {product}              | {default}      |
| size_t    | YoungPLABSize                                    |                 4096 | {product}              | {default}      |
| double    | ZAllocationSpikeTolerance                        |             2.000000 | {product}              | {default}      |
| double    | ZCollectionInterval                              |             0.000000 | {product}              | {default}      |
| double    | ZFragmentationLimit                              |            25.000000 | {product}              | {default}      |
| size_t    | ZMarkStackSpaceLimit                             |           8589934592 | {product}              | {default}      |
| bool      | ZProactive                                       |                 true | {product}              | {default}      |
| bool      | ZUncommit                                        |                 true | {product}              | {default}      |
| uintx     | ZUncommitDelay                                   |                  300 | {product}              | {default}      |
| bool      | ZeroTLAB                                         |                false | {product}              | {default}      |
