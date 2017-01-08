
# The header files will be listed in order to make sure they are
# listed and editable in all versions of the popular IDEs.
# CMake should be able to detect the header dependencies otherwise, though.
target_sources(ZCashConsensus
    PRIVATE
        "${CMAKE_CURRENT_LIST_DIR}/crypto/equihash.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/hmac_sha512.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/ripemd160.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha1.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha256.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha512.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/eccryptoverify.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/ecwrapper.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/hash.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/primitives/transaction.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/pubkey.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/zcashconsensus.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/interpreter.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/script.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/uint256.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/utilstrencodings.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/util.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/chainparamsbase.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/utiltime.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/random.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/support/cleanse.cpp"
		
		"${CMAKE_CURRENT_LIST_DIR}/zcash/IncrementalMerkleTree.hpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/NoteEncryption.hpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/Address.hpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/JoinSplit.hpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/Note.hpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/prf.h"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/Proof.hpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/util.h"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/Zcash.h"
		"${CMAKE_CURRENT_LIST_DIR}/script/zcashconsensus.h"
    PUBLIC
        "${CMAKE_CURRENT_LIST_DIR}/script/zcashconsensus.h"
)

target_sources(ZCash
	PRIVATE
		"${CMAKE_CURRENT_LIST_DIR}/zcash/IncrementalMerkleTree.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/NoteEncryption.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/Address.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/JoinSplit.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/Proof.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/Note.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/prf.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/util.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/circuit/commitment.tcc"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/circuit/gadget.tcc"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/circuit/merkle.tcc"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/circuit/note.tcc"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/circuit/prfs.tcc"
		"${CMAKE_CURRENT_LIST_DIR}/zcash/circuit/utils.tcc"
)

  
 
# find_library(BITCOIN_LIB bitcoin)
# target_link_libraries(ZCash PUBLIC ${BITCOIN_LIB})
# target_compile_definitions(ZCash PUBLIC USE_BITCOIN)
# target_include_directories(ZCash PUBLIC "${CMAKE_CURRENT_LIST_DIR}")
