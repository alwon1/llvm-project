add_mlir_conversion_library(MLIRSPIRVToLLVM
  ConvertLaunchFuncToLLVMCalls.cpp
  SPIRVToLLVM.cpp
  SPIRVToLLVMPass.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Conversion/SPIRVToLLVM

  DEPENDS
  MLIRConversionPassIncGen
  intrinsics_gen

  LINK_LIBS PUBLIC
  MLIRGPUOps
  MLIRSPIRV
  MLIRSPIRVUtils
  MLIRLLVMCommonConversion
  MLIRLLVMIR
  MLIRStandardToLLVM
  MLIRIR
  MLIRTransforms
  )
