cmake_minimum_required(VERSION 3.5)
project(fastbit)

set(CMAKE_CXX_STANDARD 11)

include_directories(src)
include_directories(win)

set(SOURCE_FILES
#    examples/ardea.cpp
#    examples/ibis.cpp
#    examples/Makefile.am
#    examples/Makefile.in
#    examples/rara.cpp
#    examples/README
#    examples/tcapi.c
#    examples/thula.cpp
#    examples/tiapi.c

        #    java/gov/lbl/fastbit/FastBit.java
#    java/gov/lbl/fastbit/FastBitStringReader.java
#    java/gov/lbl/fastbit/FastBitStringReaderException.java
#    java/gov/lbl/fastbit/FastBitStringWriter.java
#    java/gov/lbl/fastbit/FastBitStringWriterException.java
#    java/tests/lib/commons-logging.jar
#    java/tests/lib/junit-4.4.jar
#    java/tests/lib/log4j-1.2.15.jar
#    java/tests/log4j.properties
#    java/tests/README
#    java/tests/TestFastBitJava.java
#    java/build.xml
#    java/FastBit.c
#    java/FastBit.h
#    java/Makefile.am
#    java/Makefile.in
#    java/milky.java
#    java/README

    src/fastbit/array_t.cpp
    src/fastbit/array_t.h
    src/fastbit/bitvector.cpp
    src/fastbit/bitvector.h
    src/fastbit/bitvector64.cpp
    src/fastbit/bitvector64.h
    src/fastbit/blob.cpp
    src/fastbit/blob.h
    src/fastbit/bord.cpp
    src/fastbit/bord.h
    src/fastbit/bordm.cpp
    src/fastbit/bundle.cpp
    src/fastbit/bundle.h
    src/fastbit/capi.cpp
    src/fastbit/capi.h
    src/fastbit/category.cpp
    src/fastbit/category.h
    src/fastbit/column.cpp
    src/fastbit/column.h
    src/fastbit/colValues.cpp
    src/fastbit/colValues.h
    src/fastbit/const.h
    src/fastbit/countQuery.cpp
    src/fastbit/countQuery.h
    src/fastbit/dictionary.cpp
    src/fastbit/dictionary.h
    src/fastbit/Doxyfile
    src/fastbit/fastbit-config.h
    src/fastbit/fastbit-config.h.in
    src/fastbit/fileManager.cpp
    src/fastbit/fileManager.h
    src/fastbit/filter.cpp
    src/fastbit/filter.h
    src/fastbit/fromClause.cpp
    src/fastbit/fromClause.h
    src/fastbit/fromLexer.cc
    src/fastbit/fromLexer.h
    src/fastbit/fromParser.cc
    src/fastbit/fromParser.hh
    src/fastbit/horometer.h
    src/fastbit/iapi.cpp
    src/fastbit/iapi.h
    src/fastbit/ibin.cpp
    src/fastbit/ibin.h
    src/fastbit/ibis.h
    src/fastbit/icegale.cpp
    src/fastbit/icentre.cpp
    src/fastbit/icmoins.cpp
    src/fastbit/idbak.cpp
    src/fastbit/idbak2.cpp
    src/fastbit/idirekte.cpp
    src/fastbit/idirekte.h
    src/fastbit/ifade.cpp
    src/fastbit/ikeywords.cpp
    src/fastbit/ikeywords.h
    src/fastbit/imesa.cpp
    src/fastbit/index.cpp
    src/fastbit/index.h
    src/fastbit/irange.cpp
    src/fastbit/irelic.cpp
    src/fastbit/irelic.h
    src/fastbit/iroster.cpp
    src/fastbit/iroster.h
    src/fastbit/isapid.cpp
    src/fastbit/isbiad.cpp
    src/fastbit/iskive.cpp
    src/fastbit/islice.cpp
    src/fastbit/ixambit.cpp
    src/fastbit/ixbylt.cpp
    src/fastbit/ixfuge.cpp
    src/fastbit/ixfuzz.cpp
    src/fastbit/ixpack.cpp
    src/fastbit/ixpale.cpp
    src/fastbit/ixzona.cpp
    src/fastbit/ixzone.cpp
    src/fastbit/jnatural.cpp
    src/fastbit/jnatural.h
    src/fastbit/jrange.cpp
    src/fastbit/jrange.h
    src/fastbit/location.hh
    src/fastbit/mensa.cpp
    src/fastbit/mensa.h
    src/fastbit/meshQuery.cpp
    src/fastbit/meshQuery.h
    src/fastbit/part.cpp
    src/fastbit/part.h
    src/fastbit/parth.cpp
    src/fastbit/parth2d.cpp
    src/fastbit/parth3d.cpp
    src/fastbit/parth3da.cpp
    src/fastbit/parth3db.cpp
    src/fastbit/parth3dw.cpp
    src/fastbit/parti.cpp
    src/fastbit/party.cpp
    src/fastbit/position.hh
    src/fastbit/qExpr.cpp
    src/fastbit/qExpr.h
    src/fastbit/quaere.cpp
    src/fastbit/quaere.h
    src/fastbit/query.cpp
    src/fastbit/query.h
    src/fastbit/resource.cpp
    src/fastbit/resource.h
    src/fastbit/rids.cpp
    src/fastbit/rids.h
    src/fastbit/selectClause.cpp
    src/fastbit/selectClause.h
    src/fastbit/selectLexer.cc
    src/fastbit/selectLexer.h
    src/fastbit/selectParser.cc
    src/fastbit/selectParser.hh
    src/fastbit/stack.hh
    src/fastbit/tab.h
    src/fastbit/table.h
    src/fastbit/tafel.cpp
    src/fastbit/tafel.h
    src/fastbit/twister.h
    src/fastbit/util.cpp
    src/fastbit/util.h
    src/fastbit/utilidor.cpp
    src/fastbit/utilidor.h
    src/fastbit/whereClause.cpp
    src/fastbit/whereClause.h
    src/fastbit/whereLexer.cc
    src/fastbit/whereLexer.h
    src/fastbit/whereLexer.ll
    src/fastbit/whereParser.cc
    src/fastbit/whereParser.hh
    src/fastbit/whereParser.yy

#    tests/m4/libtool.m4
#    tests/m4/ltoptions.m4
#    tests/m4/ltsugar.m4
#    tests/m4/ltversion.m4
#    tests/m4/lt~obsolete.m4
#    tests/scripts/fastbit-config.in
#    tests/scripts/hcompare.pl
#    tests/scripts/jrf-check.pl
#    tests/scripts/matchCounts.pl
#    tests/scripts/printWarning.pl
#    tests/scripts/query-count.list
#    tests/scripts/star2002.sh
#    tests/vault/acmpub-0
#    tests/vault/acmpub-1
#    tests/vault/acmpub-2
#    tests/vault/hist0
#    tests/vault/hist1
#    tests/vault/hist2
#    tests/vault/hist3
#    tests/vault/hist4
#    tests/vault/hist5
#    tests/vault/hist6
#    tests/vault/inRange-1
#    tests/vault/join-1
#    tests/vault/join-2
#    tests/vault/join-3
#    tests/vault/join-4
#    tests/vault/join-5
#    tests/vault/join-6
#    tests/vault/join-7
#    tests/vault/join-8
#    tests/vault/marksdb-1
#    tests/vault/marksdb-3
#    tests/vault/marksdb-4
#    tests/vault/small-1
#    tests/vault/small-10
#    tests/vault/small-11
#    tests/vault/small-12
#    tests/vault/small-2
#    tests/vault/small-3
#    tests/vault/small-4
#    tests/vault/small-5
#    tests/vault/small-6
#    tests/vault/small-7
#    tests/vault/smatch-1
#    tests/vault/tcapi-3
#    tests/vault/text-0
#    tests/vault/thula-0
#    tests/vault/thula-1
#    tests/acmpub.csv
#    tests/acmpub.v.a
#    tests/acmpub.v.b
#    tests/inRange.cpp
#    tests/jrf.cpp
#    tests/js2.csv
#    tests/Makefile.am
#    tests/Makefile.in
#    tests/marksdb.csv
#    tests/maurel.csv
#    tests/readcsv.cpp
#    tests/README
#    tests/setqgen.cpp
#    tests/smatch.cpp
#    tests/test0.csv
#    tests/test1.csv

#    win/ardea.vcproj
#    win/dll.vcproj
#    win/FlexLexer.h
#    win/ibis.sln
#    win/ibis.vcproj
#    win/java.vcproj
#    win/MinGW.mak
#    win/README
#    win/tcapi.vcproj
#    win/thula.vcproj
#    win/trydll.cpp
#    win/trydll.vcproj
#    win/Win.mak
    )

add_library(fastbit ${SOURCE_FILES})
target_link_libraries(fastbit pthread)
target_include_directories(fastbit PUBLIC src)
