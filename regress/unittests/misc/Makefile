#	$OpenBSD: Makefile,v 1.10 2025/04/15 04:00:42 djm Exp $

PROG=test_misc
SRCS=tests.c
SRCS+=	test_convtime.c
SRCS+=	test_expand.c
SRCS+=	test_parse.c
SRCS+=	test_argv.c
SRCS+=	test_strdelim.c
SRCS+=	test_hpdelim.c
SRCS+=	test_ptimeout.c

# From usr.bin/ssh/Makefile.inc
SRCS+=	sshbuf.c
SRCS+=	sshbuf-getput-basic.c
SRCS+=	sshbuf-misc.c
SRCS+=	ssherr.c
SRCS+=	log.c
SRCS+=	xmalloc.c
SRCS+=	misc.c
SRCS+=	match.c
SRCS+=	addr.c
SRCS+=	addrmatch.c

# From usr.bin/ssh/sshd/Makefile
SRCS+=	atomicio.c cleanup.c fatal.c

REGRESS_TARGETS=run-regress-${PROG}

run-regress-${PROG}: ${PROG}
	env ${TEST_ENV} ./${PROG} ${UNITTEST_ARGS}

.include <bsd.regress.mk>
