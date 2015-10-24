#!/usr/bin/env sh

# Setup.
VERSION="0.0.1"

version() {
	printf "git-fire version %s\n" "$VERSION"

	git --version
}

# Helpers.
current_branch() {
	basename "$(git symbolic-ref HEAD)"
}

current_epoch() {
	date +%s
}

user_email() {
	git config user.email
}

new_branch() {
	echo "fire-$(current_branch)-$(user_email)-$(current_epoch)"
}

fire() {
	git checkout -b "$(new_branch)"
    
	# cd to git root directory
	cd "$(git rev-parse --show-toplevel)"

	git add -A

	if [ -z "$1" ]; then
		message="Fire! Branch $(current_branch)."
	else
		message="$*"
	fi

	git commit -m "$message" --no-verify

	for remote in $(git remote); do
		git push --set-upstream "${remote}" "$(current_branch)" || true
	done

	printf "\n\nLeave building!\n"
}

display_help() {
	cat <<-EOF

  usage:
    git fire [options] [COMMAND] [args]

  commands:
    git fire                        Add, commit, and push to remote in case of a fire
    git fire <message>              Execute git fire with <message> for commit message


  options:
    -V, --version                   Output current version of git-fire
    -h, --help                      Display this help information

EOF
	exit 0
}


case $1 in
	-V|--version) version; exit 0 ;;
	-h|--help) display_help; exit 0 ;;
esac

fire "$@"
