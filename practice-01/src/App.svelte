<script>
  import Header from "./UI/Header.svelte";
  import MeetupItem from "./Meetups/MeetupItem.svelte";

  const meetups = [
    {
      id: "m1",
      title: "Coding Bootcamp",
      subtitle: "Learn to code in 2 hours",
      description:
        "In this meetup, we will have some experts that teach you how to code!",
      imageUrl: "",
      address: "27th Nerd Road, 32523 New York",
      contactEmail: "code@test.com",
    },
    {
      id: "m2",
      title: "Swim Together",
      subtitle: "Let's go for some swimming",
      description: "We will simply swim some rounds!",
      imageUrl: "",
      address: "27th Nerd Road, 32523 New York",
      contactEmail: "swim@test.com",
    },
  ];
</script>

<Header />

<section id="meetups">
  {#each meetups as meetup}
    <MeetupItem
      title={meetup.title}
      subTitle={meetup.subtitle}
      description={meetup.description}
      imageUrl={meetup.imageUrl}
      address={meetup.address}
      email={meetup.contactEmail}
    />
  {/each}
</section>

<style>
  #meetups {
    margin-top: 5rem;
  }
</style>
