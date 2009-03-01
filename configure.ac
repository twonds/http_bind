AC_INIT([mod_http_bind], [master], [tofu@thetofu.com])
AM_INIT_AUTOMAKE

AC_ERLANG_NEED_ERLC
AC_ERLANG_NEED_ERL

ERLCFLAGS="$ERLCFLAGS -I $prefix/lib/ejabberd/include\
 -I $prefix/lib/ejabberd/include/web\
 -pz $prefix/lib/ejabberd/ebin"
ERLFLAGS="$ERLFLAGS -pz $prefix/lib/ejabberd/ebin"

ERL_CHECK_HEADER(ejabberd.hrl, [], 
			     [AC_MSG_ERROR([ejabberd.hrl is required.  Make sure PREFIX is the same as the PREFIX at which ejabberd is installed.])])

ERL_CHECK_HEADER(ejabberd_http.hrl, [], 
			     [AC_MSG_ERROR([ejabberd_http.hrl is required.  Make sure PREFIX is the same as the PREFIX at which ejabberd is installed.])])

ERL_CHECK_HEADER(jlib.hrl, [], 
			     [AC_MSG_ERROR([jlib.hrl is required.  Make sure PREFIX is the same as the PREFIX at which ejabberd is installed.])])

ERL_CHECK_MODULE(gen_mod, [],
		 [AC_MSG_ERROR([gen_mod module is required.  Make sure PREFIX is the same as the PREFIX at which ejabberd is installed.])])

AC_SUBST(ERLCFLAGS)			 
AC_CONFIG_FILES([Makefile])
AC_OUTPUT
