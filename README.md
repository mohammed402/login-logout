# login-logout
signInWithFB(): void {
  this.authService.signIn(FacebookLoginProvider.PROVIDER_ID);
}

signOut(): void {
  this.authService.signOut();
}
ngOnInit() {
  this.authService.authState.subscribe((user) => {
    this.user = user;
    this.loggedIn = (user != null);
    console.log(this.user);
  });
}
