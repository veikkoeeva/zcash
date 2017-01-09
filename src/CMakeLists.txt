# The header files will be listed in order to make sure they are
# listed and editable in all versions of the popular IDEs.
# CMake should be able to detect the header dependencies by itself.

# This is LIBZCASH_H from Makefile.am.
set(ZCashHeaders		
	"${CMAKE_CURRENT_LIST_DIR}/zcash/IncrementalMerkleTree.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/NoteEncryption.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/Address.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/JoinSplit.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/Note.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/prf.h"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/Proof.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/util.h"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/Zcash.h"
)

# This is BITCOIN_CORE_H from Makefile.am.
set(BitcoinCoreHeaders
	"${CMAKE_CURRENT_LIST_DIR}/addrman.h"
	"${CMAKE_CURRENT_LIST_DIR}/alert.h"
	"${CMAKE_CURRENT_LIST_DIR}/amount.h"
	"${CMAKE_CURRENT_LIST_DIR}/arith_uint256.h"
	"${CMAKE_CURRENT_LIST_DIR}/asyncrpcoperation.h"
	"${CMAKE_CURRENT_LIST_DIR}/asyncrpcqueue.h"
	"${CMAKE_CURRENT_LIST_DIR}/base58.h"
	"${CMAKE_CURRENT_LIST_DIR}/bloom.h"
	"${CMAKE_CURRENT_LIST_DIR}/chain.h"
	"${CMAKE_CURRENT_LIST_DIR}/chainparams.h"
	"${CMAKE_CURRENT_LIST_DIR}/chainparamsbase.h"
	"${CMAKE_CURRENT_LIST_DIR}/chainparamsseeds.h"
	"${CMAKE_CURRENT_LIST_DIR}/checkpoints.h"
	"${CMAKE_CURRENT_LIST_DIR}/checkqueue.h"
	"${CMAKE_CURRENT_LIST_DIR}/clientversion.h"
	"${CMAKE_CURRENT_LIST_DIR}/coincontrol.h"
	"${CMAKE_CURRENT_LIST_DIR}/coins.h"
	"${CMAKE_CURRENT_LIST_DIR}/compat.h"
	"${CMAKE_CURRENT_LIST_DIR}/compat/byteswap.h"
	"${CMAKE_CURRENT_LIST_DIR}/compat/endian.h"
	"${CMAKE_CURRENT_LIST_DIR}/compat/sanity.h"
	"${CMAKE_CURRENT_LIST_DIR}/compressor.h"
	"${CMAKE_CURRENT_LIST_DIR}/consensus/consensus.h"
	"${CMAKE_CURRENT_LIST_DIR}/consensus/params.h"
	"${CMAKE_CURRENT_LIST_DIR}/consensus/validation.h"
	"${CMAKE_CURRENT_LIST_DIR}/core_io.h"
	"${CMAKE_CURRENT_LIST_DIR}/eccryptoverify.h"
	"${CMAKE_CURRENT_LIST_DIR}/ecwrapper.h"
	"${CMAKE_CURRENT_LIST_DIR}/hash.h"
	"${CMAKE_CURRENT_LIST_DIR}/init.h"
	"${CMAKE_CURRENT_LIST_DIR}/key.h"
	"${CMAKE_CURRENT_LIST_DIR}/keystore.h"
	"${CMAKE_CURRENT_LIST_DIR}/leveldbwrapper.h"
	"${CMAKE_CURRENT_LIST_DIR}/limitedmap.h"
	"${CMAKE_CURRENT_LIST_DIR}/main.h"
	"${CMAKE_CURRENT_LIST_DIR}/memusage.h"
	"${CMAKE_CURRENT_LIST_DIR}/merkleblock.h"
	"${CMAKE_CURRENT_LIST_DIR}/metrics.h"
	"${CMAKE_CURRENT_LIST_DIR}/miner.h"
	"${CMAKE_CURRENT_LIST_DIR}/mruset.h"
	"${CMAKE_CURRENT_LIST_DIR}/net.h"
	"${CMAKE_CURRENT_LIST_DIR}/netbase.h"
	"${CMAKE_CURRENT_LIST_DIR}/noui.h"
	"${CMAKE_CURRENT_LIST_DIR}/policy/fees.h"
	"${CMAKE_CURRENT_LIST_DIR}/pow.h"
	"${CMAKE_CURRENT_LIST_DIR}/primitives/block.h"
	"${CMAKE_CURRENT_LIST_DIR}/primitives/transaction.h"
	"${CMAKE_CURRENT_LIST_DIR}/protocol.h"
	"${CMAKE_CURRENT_LIST_DIR}/pubkey.h"
	"${CMAKE_CURRENT_LIST_DIR}/random.h"
	"${CMAKE_CURRENT_LIST_DIR}/reverselock.h"
	"${CMAKE_CURRENT_LIST_DIR}/rpcclient.h"
	"${CMAKE_CURRENT_LIST_DIR}/rpcprotocol.h"
	"${CMAKE_CURRENT_LIST_DIR}/rpcserver.h"
	"${CMAKE_CURRENT_LIST_DIR}/scheduler.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/interpreter.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/script.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/script_error.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/sigcache.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/sign.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/standard.h"
	"${CMAKE_CURRENT_LIST_DIR}/serialize.h"
	"${CMAKE_CURRENT_LIST_DIR}/streams.h"
	"${CMAKE_CURRENT_LIST_DIR}/support/allocators/secure.h"
	"${CMAKE_CURRENT_LIST_DIR}/support/allocators/zeroafterfree.h"
	"${CMAKE_CURRENT_LIST_DIR}/support/cleanse.h"
	"${CMAKE_CURRENT_LIST_DIR}/support/pagelocker.h"
	"${CMAKE_CURRENT_LIST_DIR}/sync.h"
	"${CMAKE_CURRENT_LIST_DIR}/threadsafety.h"
	"${CMAKE_CURRENT_LIST_DIR}/timedata.h"
	"${CMAKE_CURRENT_LIST_DIR}/tinyformat.h"
	"${CMAKE_CURRENT_LIST_DIR}/txdb.h"
	"${CMAKE_CURRENT_LIST_DIR}/txmempool.h"
	"${CMAKE_CURRENT_LIST_DIR}/ui_interface.h"
	"${CMAKE_CURRENT_LIST_DIR}/uint256.h"
	"${CMAKE_CURRENT_LIST_DIR}/uint252.h"
	"${CMAKE_CURRENT_LIST_DIR}/undo.h"
	"${CMAKE_CURRENT_LIST_DIR}/util.h"
	"${CMAKE_CURRENT_LIST_DIR}/utilmoneystr.h"
	"${CMAKE_CURRENT_LIST_DIR}/utilstrencodings.h"
	"${CMAKE_CURRENT_LIST_DIR}/utiltime.h"
	"${CMAKE_CURRENT_LIST_DIR}/validationinterface.h"
	"${CMAKE_CURRENT_LIST_DIR}/version.h"
	"${CMAKE_CURRENT_LIST_DIR}/wallet/asyncrpcoperation_sendmany.h"
	"${CMAKE_CURRENT_LIST_DIR}/wallet/crypter.h"
	"${CMAKE_CURRENT_LIST_DIR}/wallet/db.h"
	"${CMAKE_CURRENT_LIST_DIR}/wallet/wallet.h"
	"${CMAKE_CURRENT_LIST_DIR}/wallet/wallet_ismine.h"
	"${CMAKE_CURRENT_LIST_DIR}/wallet/walletdb.h"
)

# This is JSON_H from Makefile.am.
set(JsonHeaders
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit.h"
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit_error_position.h"
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit_reader.h"
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit_reader_template.h"
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit_stream_reader.h"
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit_utils.h"
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit_value.h"
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit_writer.h"
	"${CMAKE_CURRENT_LIST_DIR}/json/json_spirit_writer_template.h"
)

set(ZCashConsensusHeaders
	"${CMAKE_CURRENT_LIST_DIR}/crypto/equihash.h"
	"${CMAKE_CURRENT_LIST_DIR}/crypto/hmac_sha512.h"
	"${CMAKE_CURRENT_LIST_DIR}/crypto/ripemd160.h"
	"${CMAKE_CURRENT_LIST_DIR}/crypto/sha1.h"
	"${CMAKE_CURRENT_LIST_DIR}/crypto/sha256.h"
	"${CMAKE_CURRENT_LIST_DIR}/crypto/sha512.h"
	"${CMAKE_CURRENT_LIST_DIR}/eccryptoverify.h"
	"${CMAKE_CURRENT_LIST_DIR}/ecwrapper.h"
	"${CMAKE_CURRENT_LIST_DIR}/hash.h"
	"${CMAKE_CURRENT_LIST_DIR}/primitives/transaction.h"
	"${CMAKE_CURRENT_LIST_DIR}/pubkey.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/zcashconsensus.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/interpreter.h"
	"${CMAKE_CURRENT_LIST_DIR}/script/script.h"
	"${CMAKE_CURRENT_LIST_DIR}/uint256.h"
	"${CMAKE_CURRENT_LIST_DIR}/utilstrencodings.h"
	"${CMAKE_CURRENT_LIST_DIR}/util.h"
	"${CMAKE_CURRENT_LIST_DIR}/chainparamsbase.h"
	"${CMAKE_CURRENT_LIST_DIR}/utiltime.h"
	"${CMAKE_CURRENT_LIST_DIR}/random.h"
	"${CMAKE_CURRENT_LIST_DIR}/support/cleanse.h"
				
	"${CMAKE_CURRENT_LIST_DIR}/zcash/IncrementalMerkleTree.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/NoteEncryption.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/Address.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/JoinSplit.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/Note.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/prf.h"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/Proof.hpp"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/util.h"
	"${CMAKE_CURRENT_LIST_DIR}/zcash/Zcash.h"
)

# This is libbitcoin_server from Makefile.am.
target_sources(BitcoinServer
	PRIVATE									
		"${CMAKE_CURRENT_LIST_DIR}/sendalert.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/addrman.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/alert.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/alertkeys.h"
		"${CMAKE_CURRENT_LIST_DIR}/asyncrpcoperation.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/asyncrpcqueue.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/bloom.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/chain.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/checkpoints.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/init.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/leveldbwrapper.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/main.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/merkleblock.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/metrics.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/miner.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/net.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/noui.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/policy/fees.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/pow.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/rest.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/rpcblockchain.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/rpcmining.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/rpcmisc.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/rpcnet.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/rpcrawtransaction.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/rpcserver.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/sigcache.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/timedata.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/txdb.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/txmempool.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/validationinterface.cpp"
		${JsonHeaders}
		${BitcoinCoreHeaders}
		${ZCashHeaders}
)

target_sources(BitcoinWallet
	PRIVATE		
		"${CMAKE_CURRENT_LIST_DIR}/utiltest.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/utiltest.h"
		"${CMAKE_CURRENT_LIST_DIR}/zcbenchmarks.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/zcbenchmarks.h"
		"${CMAKE_CURRENT_LIST_DIR}/wallet/asyncrpcoperation_sendmany.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/wallet/crypter.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/wallet/db.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/wallet/rpcdump.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/wallet/rpcwallet.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/wallet/wallet.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/wallet/wallet_ismine.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/wallet/walletdb.cpp"
		${BitcoinCoreHeaders}
		${ZCashHeaders}
)


# target_sources(EquihashTromp PROPERTIES LINKER_LANGUAGE CXX
#	PRIVATE		
#		"${CMAKE_CURRENT_LIST_DIR}/pow/tromp/equi_miner.h"
#		"${CMAKE_CURRENT_LIST_DIR}/pow/tromp/equi.h"
#		"${CMAKE_CURRENT_LIST_DIR}/pow/tromp/osx_barrier.h"
# )

target_sources(Bitcoin
	PRIVATE		
		"${CMAKE_CURRENT_LIST_DIR}/crypto/common.h"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/equihash.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/equihash.h"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/equihash.tcc"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/hmac_sha256.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/hmac_sha256.h"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/hmac_sha512.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/hmac_sha512.h"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/ripemd160.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/ripemd160.h"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha1.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha1.h"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha256.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha256.h"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha512.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/crypto/sha512.h"
		
		"${CMAKE_CURRENT_LIST_DIR}/pow/tromp/equi_miner.h"
		"${CMAKE_CURRENT_LIST_DIR}/pow/tromp/equi.h"
		"${CMAKE_CURRENT_LIST_DIR}/pow/tromp/osx_barrier.h"
		
		#${EquihashTromp}
)

target_sources(UnivalueBitcoin
	PRIVATE	
		"${CMAKE_CURRENT_LIST_DIR}/univalue/univalue.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/univalue/univalue.h"
		"${CMAKE_CURRENT_LIST_DIR}/univalue/univalue_escapes.h"
		"${CMAKE_CURRENT_LIST_DIR}/univalue/univalue_read.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/univalue/univalue_write.cpp"
)


target_sources(BitcoinCommon
	PRIVATE	
		"${CMAKE_CURRENT_LIST_DIR}/amount.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/arith_uint256.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/base58.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/chainparams.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/coins.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/compressor.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/core_read.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/core_write.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/eccryptoverify.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/ecwrapper.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/hash.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/key.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/keystore.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/netbase.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/primitives/block.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/primitives/transaction.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/protocol.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/pubkey.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/scheduler.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/interpreter.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/script.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/script_error.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/sign.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/script/standard.cpp"
		${BitcoinCoreHeaders}
		${ZCashHeaders}
 )


 target_sources(BitcoinUtil
	PRIVATE	
		"${CMAKE_CURRENT_LIST_DIR}/support/pagelocker.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/chainparamsbase.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/clientversion.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/compat/glibc_sanity.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/compat/glibcxx_sanity.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/compat/strnlen.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/random.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/rpcprotocol.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/support/cleanse.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/sync.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/uint256.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/util.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/utilmoneystr.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/utilstrencodings.cpp"
		"${CMAKE_CURRENT_LIST_DIR}/utiltime.cpp"
		${BitcoinCoreHeaders}
		${ZCashConsensusHeaders}
)

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
		${ZCashConsensusHeaders}					
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
				
		"${CMAKE_CURRENT_LIST_DIR}/uint256.h"
		"${CMAKE_CURRENT_LIST_DIR}/serialize.h"
)
 
# find_library(BITCOIN_LIB bitcoin)
# target_link_libraries(ZCash PUBLIC ${BITCOIN_LIB})
# target_compile_definitions(ZCash PUBLIC USE_BITCOIN)
# target_include_directories(ZCash PUBLIC "${CMAKE_CURRENT_LIST_DIR}")
