<template>

  <PageTemplate :completed="false">

    <PageSection>
      <h3>Code Example</h3>
      <VueExample :code="ExampleCode">
        <Example />
      </VueExample>

      <h3>Guidelines</h3>
      <p>TODO</p>
    </PageSection>

  </PageTemplate>

</template>


<script>

  /* eslint-disable import/no-duplicates */
  import Example from './Example';
  import PageTemplate from '~/common/PageTemplate';
  import PageSection from '~/common/PageSection';
  import VueExample from '~/common/VueExample';

  import ExampleCode from '!!raw-loader!./Example';
  // import KCircularLoaderApi from '!vue-doc!~~/lib/loaders/KCircularLoader';
  /* eslint-enable import/no-duplicates */

  export default {
    name: 'KCircularLoader',
    components: {
      PageTemplate,
      PageSection,
      VueExample,
      Example,
    },
    data: () => ({
      ExampleCode,
      KCircularLoaderApi: {}, // TODO
    }),
  };

</script>


<style lang="scss" scoped></style>
