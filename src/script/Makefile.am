lib_LTLIBRARIES += lib/libCsScript@BUILD_ABI@.la
lib_libCsScript@BUILD_ABI@_la_SOURCES =

lib_libCsScript@BUILD_ABI@_la_CXXFLAGS = $(AM_CXXFLAGS) -Iinclude -Iinclude/QtCore -Iinclude/QtScript \
	-Iprivateinclude/QtCore \
	-Iprivateinclude/QtScript \
	-Iprivateinclude/QtScript/private \
	-DQT_BUILD_SCRIPT_LIB \
	-DQLALR_NO_SCRIPTGRAMMAR_DEBUG_INFO -DJS_NO_EXPORT \
	-I$(top_srcdir)/src/3rdparty/javascriptcore \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/API \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/assembler \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/bytecode \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/bytecompiler \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/debugger \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/generated \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/heap \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/interpreter \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/jit \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/parser \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/pcre \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/profiler \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/runtime \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/unicode \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/wrec \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/wtf \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode \
	-I$(top_srcdir)/src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders \
	-I$(top_srcdir)/src/script \
	-Isrc/3rdparty/javascriptcore/JavaScriptCore/wtf/qt \
	-Isrc/script/api \
	-Isrc/script/bridge \
	-DQLALR_NO_QSCRIPTGRAMMAR_DEBUG_INFO \
	-DWTF_USE_JAVASCRIPTCORE_BINDINGS=1 \
	-DWTF_CHANGES=1 \
	-DJS_NO_EXPORT \
	-DBUILDING_QT__=1 \
	-DWTF_USE_ACCELERATED_COMPOSITING \
	-DJSC=QTJSC -Djscyyparse=qtjscyyparse -Djscyylex=qtjscyylex \
	-Djscyyerror=qtjscyyerror \
	-DWTF=QTWTF \
	-UHAVE_CONFIG_H \
	-DUSE_SYSTEM_MALLOC  \
	-DQT_BUILD_SCRIPT_LIB

#	-DWTF_USE_JAVASCRIPTCORE_BINDINGS=1 -DWTF_CHANGES=1
#	-DBUILDING_QT__
#	-DBUILDING_JavaScriptCore -DBUILDING_WTF
#	-DJSC=QTJSC -Djscyyparse=qtjscyyparse -Djscyylex=qtjscyylex
#	-Djscyyerror=qtjscyyerror -DWTF=QTWTF -DWTF_EXPORT_PRIVATE=""
#	-DWTF_USE_JSC -DWTF_PLATFORM_QT=1

lib_libCsScript@BUILD_ABI@_la_LDFLAGS = $(AM_LDFLAGS) -no-undefined
lib_libCsScript@BUILD_ABI@_la_LIBADD = lib/libCsCore@BUILD_ABI@.la


if OSTYPE_WIN
lib_libCsScript@BUILD_ABI@_la_LDFLAGS += -lwinmm
endif

if OSTYPE_DARWIN
lib_libCsScript@BUILD_ABI@_la_CXXFLAGS += -DENABLE_JSC_MULTIPLE_THREADS=0
endif

SCRIPT_INCLUDES =
SCRIPT_PUBLIC_INCLUDES =
SCRIPT_PRIVATE_INCLUDES =
SCRIPT_DIRS =

EXTRA_DIST += \
	src/script/CMakeLists.txt \
	src/script/api/api.cmake \
	src/script/bridge/bridge.cmake \
	src/script/parser/parser.cmake

include src/script/api/Makefile.am
include src/script/bridge/Makefile.am
include src/script/parser/Makefile.am

noinst_HEADERS += \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/CodeBlock.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/Opcode.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/SamplingTool.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/JumpTable.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/Instruction.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/StructureStubInfo.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/EvalCodeCache.h \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/pcre_internal.h \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/ucpinternal.h \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/pcre.h \
	src/3rdparty/javascriptcore/JavaScriptCore/config.h \
	src/3rdparty/javascriptcore/JavaScriptCore/JavaScriptCorePrefix.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/OpaqueJSString.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSStringRefBSTR.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JavaScript.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSValueRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSCallbackFunction.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/APICast.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSObjectRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSBasePrivate.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSContextRefPrivate.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSCallbackObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSContextRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSStringRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/WebKitAvailability.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSClassRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSBase.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/APIShims.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSStringRefCF.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSCallbackConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSProfilerPrivate.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSRetainPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSCallbackObjectFunctions.h \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JavaScriptCore.h \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/Interpreter.h \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/CallFrameClosure.h \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/RegisterFile.h \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/Register.h \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/CachedCall.h \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/CallFrame.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/ArrayPrototype.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/RegExpConstructor.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/RegExpObject.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/Grammar.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/GeneratedJITStubs_RVCT.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/MathObject.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/JSONObject.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/Lexer.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/NumberConstructor.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/StringPrototype.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/DatePrototype.lut.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wrec/WRECParser.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wrec/CharacterClassConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wrec/Escapes.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wrec/CharacterClass.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wrec/Quantifier.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wrec/WRECFunctors.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wrec/WRECGenerator.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wrec/WREC.h \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITInlineMethods.h \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/ExecutableAllocator.h \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITStubs.h \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITCode.h \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITStubCall.h \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JIT.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/OpaqueJSString.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JavaScript.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JSValueRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/APICast.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JSObjectRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JSContextRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JSStringRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/WebKitAvailability.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JSBase.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JSStringRefCF.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JSRetainPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/ForwardingHeaders/JavaScriptCore/JavaScriptCore.h \
	src/3rdparty/javascriptcore/JavaScriptCore/os-win32/stdbool.h \
	src/3rdparty/javascriptcore/JavaScriptCore/os-win32/stdint.h \
	src/3rdparty/javascriptcore/JavaScriptCore/debugger/Debugger.h \
	src/3rdparty/javascriptcore/JavaScriptCore/debugger/DebuggerActivation.h \
	src/3rdparty/javascriptcore/JavaScriptCore/debugger/DebuggerCallFrame.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecompiler/Label.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecompiler/LabelScope.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecompiler/RegisterID.h \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecompiler/BytecodeGenerator.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/CodeLocation.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/ARMAssembler.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/MacroAssemblerCodeRef.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/AssemblerBuffer.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/MacroAssemblerX86_64.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/ARMv7Assembler.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/LinkBuffer.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/RepatchBuffer.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/MacroAssemblerARM.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/MacroAssemblerX86Common.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/MacroAssemblerARMv7.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/MacroAssembler.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/AssemblerBufferWithConstantPool.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/AbstractMacroAssembler.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/MacroAssemblerX86.h \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/X86Assembler.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ClassInfo.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ArgList.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/TimeoutChecker.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NumberConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSGlobalData.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Identifier.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/BooleanPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DateConversion.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DateConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSZombie.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/WeakRandom.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/FunctionConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/CollectorHeapIterator.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ScopeChainMark.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSGlobalObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/BatchedTransitionOptimizer.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSVariableObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PropertyDescriptor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/BooleanConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Completion.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Structure.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/SymbolTable.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/MarkStack.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ErrorPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSType.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DatePrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ObjectConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSArray.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NumericStrings.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSActivation.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StringConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSImmediate.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSONObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ObjectPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NativeErrorPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ArrayConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSValue.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DateInstance.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSAPIValueWrapper.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NativeFunctionWrapper.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSGlobalObjectFunctions.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StringPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExpMatchesArray.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSByteArray.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Error.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/InitializeThreading.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Collector.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ArrayPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PropertyMapHashTable.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSTypeInfo.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StructureTransitionTable.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NumberPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExpConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Tracing.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/UStringImpl.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/GetterSetter.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NumberObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Executable.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSPropertyNameIterator.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Lookup.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/UString.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/MathObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/SmallStrings.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExpObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/FunctionPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/InternalFunction.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExpPrototype.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/BooleanObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Protect.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Arguments.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StructureChain.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSFunction.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/WeakGCMap.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSLock.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PropertySlot.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSNumberCell.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Operations.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NativeErrorConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ConstructData.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StringObjectThatMasqueradesAsUndefined.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ScopeChain.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ErrorInstance.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/LiteralParser.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSCell.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ExceptionHelpers.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PrototypeFunction.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/WeakGCPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PropertyNameArray.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSString.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/GlobalEvalFunction.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DateInstanceCache.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StringBuilder.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PutPropertySlot.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ErrorConstructor.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSStaticScopeObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSWrapperObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/CommonIdentifiers.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSNotAnObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExp.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/CallData.h \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StringObject.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/SourceProvider.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/ResultType.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/ParserArena.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/Nodes.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/NodeInfo.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/Lexer.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/SourceCode.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/NodeConstructors.h \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/Parser.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/ThreadSpecific.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RefCountedLeakCounter.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/PassRefPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/HashFunctions.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/HashMap.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/HashIterators.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/SegmentedVector.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Vector.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/TypeTraits.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/TCPackedCache.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/ASCIICType.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/android/AndroidThreading.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/dtoa.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RefPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/TCSpinLock.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/OwnArrayPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Platform.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/PossiblyNull.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/MessageQueue.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Forward.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/TCSystemAlloc.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/StringHashFunctions.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/CurrentTime.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/MainThread.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/FastAllocBase.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/CrossThreadRefCounted.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/MathExtras.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Threading.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/StdLibExtras.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RandomNumberSeed.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RandomNumber.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/DateMath.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/PtrAndFlags.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/GetPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/ByteArray.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/OwnPtrCommon.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/ListRefPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/HashTraits.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/VectorTraits.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/AVLTree.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Assertions.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/Collator.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/qt4/UnicodeQt4.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/glib/UnicodeGLib.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/glib/UnicodeMacrosFromICU.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/UTF8.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/icu/UnicodeIcu.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/Unicode.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Locker.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/StringExtras.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/DisallowCType.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/FastMalloc.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RefCounted.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/HashTable.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/MallocZoneSupport.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/OwnPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Deque.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Noncopyable.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/TCPageMap.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/HashSet.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RefPtrHashMap.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/ThreadIdentifierDataPthreads.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/PassOwnPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/NotFound.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/VMTags.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RetainPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/OwnFastMallocPtr.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/AlwaysInline.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/HashCountedSet.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/UnusedParam.h \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/ListHashSet.h \
	src/3rdparty/javascriptcore/JavaScriptCore/yarr/RegexJIT.h \
	src/3rdparty/javascriptcore/JavaScriptCore/yarr/RegexInterpreter.h \
	src/3rdparty/javascriptcore/JavaScriptCore/yarr/RegexPattern.h \
	src/3rdparty/javascriptcore/JavaScriptCore/yarr/RegexParser.h \
	src/3rdparty/javascriptcore/JavaScriptCore/yarr/RegexCompiler.h \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/Profiler.h \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/Profile.h \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/ProfileGenerator.h \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/ProfileNode.h \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/ProfilerServer.h \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/CallIdentifier.h \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/chartables.c \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/ucptable.cpp


lib_libCsScript@BUILD_ABI@_la_SOURCES += \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSBase.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSCallbackConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSCallbackFunction.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSCallbackObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSClassRef.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSContextRef.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSObjectRef.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSStringRef.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/JSValueRef.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/API/OpaqueJSString.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/ARMAssembler.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/assembler/MacroAssemblerARM.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/CodeBlock.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/JumpTable.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/Opcode.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/SamplingTool.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecode/StructureStubInfo.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecompiler/BytecodeGenerator.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/bytecompiler/NodesCodegen.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/debugger/DebuggerActivation.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/debugger/DebuggerCallFrame.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/debugger/Debugger.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/CallFrame.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/Interpreter.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/interpreter/RegisterFile.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/ExecutableAllocatorFixedVMPool.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/ExecutableAllocatorPosix.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/ExecutableAllocatorWin.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/ExecutableAllocator.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITArithmetic.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITCall.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JIT.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITOpcodes.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITPropertyAccess.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/jit/JITStubs.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/Lexer.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/Nodes.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/ParserArena.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/parser/Parser.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/Profile.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/ProfileGenerator.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/ProfileNode.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/profiler/Profiler.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ArgList.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Arguments.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ArrayConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ArrayPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/BooleanConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/BooleanObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/BooleanPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/CallData.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Collector.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/CommonIdentifiers.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Completion.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ConstructData.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DateConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DateConversion.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DateInstance.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/DatePrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ErrorConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Error.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ErrorInstance.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ErrorPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ExceptionHelpers.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Executable.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/FunctionConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/FunctionPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/GetterSetter.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/GlobalEvalFunction.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Identifier.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/InitializeThreading.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/InternalFunction.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSActivation.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSAPIValueWrapper.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSArray.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSByteArray.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSCell.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSFunction.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSGlobalData.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSGlobalObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSGlobalObjectFunctions.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSImmediate.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSLock.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSNotAnObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSNumberCell.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSONObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSPropertyNameIterator.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSStaticScopeObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSString.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSValue.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSVariableObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/JSWrapperObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/LiteralParser.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Lookup.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/MarkStackPosix.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/MarkStackWin.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/MarkStack.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/MathObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NativeErrorConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NativeErrorPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NumberConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NumberObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/NumberPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ObjectConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ObjectPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Operations.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PropertyDescriptor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PropertyNameArray.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PropertySlot.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/PrototypeFunction.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExpConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExp.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExpObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/RegExpPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/ScopeChain.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/SmallStrings.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StringConstructor.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StringObject.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StringPrototype.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/StructureChain.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/Structure.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/TimeoutChecker.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/UString.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/runtime/UStringImpl.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Assertions.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/ByteArray.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/CurrentTime.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/DateMath.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/dtoa.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/FastMalloc.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/HashTable.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/MainThread.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/qt/MainThreadQt.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/qt/ThreadingQt.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RandomNumber.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/RefCountedLeakCounter.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/ThreadingNone.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/Threading.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/TypeTraits.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/CollatorDefault.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/icu/CollatorICU.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/wtf/unicode/UTF8.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/yarr/RegexCompiler.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/yarr/RegexInterpreter.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/yarr/RegexJIT.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/generated/Grammar.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/pcre_compile.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/pcre_exec.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/pcre_tables.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/pcre_ucp_searchfuncs.cpp \
	src/3rdparty/javascriptcore/JavaScriptCore/pcre/pcre_xclass.cpp

SCRIPT_HEADERS_INSTALLED= \
	$(patsubst %,include/QtScript/%,$(SCRIPT_INCLUDES)) \
	$(patsubst %,include/QtScript/%,$(SCRIPT_PUBLIC_INCLUDES)) \
	$(patsubst %,privateinclude/QtScript/private/%,$(SCRIPT_PRIVATE_INCLUDES)) \
	include/QtScript privateinclude/QtScript/private

BUILT_SOURCES+=.script-header-deps.mk

$(lib_libCsScript@BUILD_ABI@_la_SOURCES) : $(CORE_HEADERS_INSTALLED) $(SCRIPT_HEADERS_INSTALLED)

-include .script-header-deps.mk

.script-header-deps.mk: Makefile
	@- rm -rf $@
	echo "include/QtScript:" >> $@; \
	echo "	\$$(MKDIR_P) \$$@" >> $@ ; \
	echo "privateinclude/QtScript/private:" >> $@; \
	echo "	\$$(MKDIR_P) \$$@" >> $@ ; \
	for i in $(SCRIPT_PUBLIC_INCLUDES); do \
		echo "include/QtScript/$$i: include/QtScript/$$(echo $$i | tr A-Z a-z).h | include/QtScript" >> $@; \
		echo "	\$$(INSTALL) \$$< \$$@" >> $@ ; \
	done; \
	for i in $(SCRIPT_DIRS); do \
		echo "include/QtScript/%: $$i/% | include/QtScript" >> $@ ; \
		echo "	\$$(INSTALL) \$$< \$$@" >> $@ ; \
	done;\
	for i in $(SCRIPT_DIRS); do \
		echo "privateinclude/QtScript/private/%: $$i/% | privateinclude/QtScript/private" >> $@ ; \
		echo "	\$$(INSTALL) \$$< \$$@" >> $@ ; \
	done
